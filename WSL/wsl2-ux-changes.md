---
title: WSL 1 和 WSL 2 之間的 UX 變更
description: WSL 1 與 WSL 2 之間的使用者體驗變更
keywords: BashOnWindows, bash, wsl, wsl2, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a6c8f4fbbf21b4295e69fe3de2ecf0922ab20bbe
ms.sourcegitcommit: 6086126c35a5518a7110935fa13592b5ed9dd6b7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/15/2019
ms.locfileid: "67891780"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 與 WSL 2 之間的使用者體驗變更


此頁面會介紹 WSL 1 與 WSL 2 預覽版之間的使用者體驗差異。要注意的關鍵變更如下：


- 將您的 Linux 應用程式將在 Linux 根檔案系統中存取的檔案放在一起, 以加快檔案效能速度
- 在 WSL 2 preview 的初始組建中, 您將需要使用 IP 位址存取網路應用程式, 而不使用 localhost

以下是您可能會注意到的其他變更的完整清單:

- WSL 2 使用[虛擬硬體磁片](https://en.wikipedia.org/wiki/VHD_(file_format))(VHD) 來儲存您的檔案, 如果您達到其大小上限, 您可能需要將它展開
- 啟動時, WSL 2 現在會使用一小部分的記憶體
- 初次預覽組建中的跨 OS 檔案存取速度會變慢

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>將您的 Linux 檔案放在 Linux 根檔案系統中
請務必將您將經常使用 Linux 應用程式存取的檔案放在 Linux 根檔案系統內，以享有檔案效能優勢。這些檔案必須位於 Linux 根檔案系統內，才能加快檔案系統存取的速度。我們也讓 Windows 應用程式可以存取 Linux 根檔案系統 (例如，檔案總管！請嘗試執行 Linux 發行版本主目錄中的 `explorer.exe`，並查看發生什麼事)，這將會大幅簡化此轉換。

## <a name="accessing-network-applications"></a>存取網路應用程式

在 WSL 2 預覽版的初始組建中，您將必須使用您 Linux 發行版本的 IP 位址來存取來自 Windows 的任何 Linux 伺服器，以及使用您主機電腦的 IP 位址存取來自 Linux 的任何 Windows 伺服器。這是暫時性問題，而且這在我們的修正順序清單中的順位非常高。

### <a name="accessing-linux-applications-from-windows"></a>從 Windows 存取 Linux 應用程式
如果您在 WSL 發行版本中有一部伺服器，您將必須尋找裝載您發行版本之虛擬機器的 IP 位址，並使用該 IP 位址來連線到您的發行版本。您可以遵循下列步驟來執行此動作：

- 在您的 WSL 發行版本內執行命令 `ip addr`，並在 `eth0` 介面的 `inet` 值底下尋找它，以取得發行版本的 IP 位址。
   - 使用 grep 篩選命令的輸出 (如下所示), 可以更輕鬆地找到此`ip addr | grep eth0`程式:。
- 使用您在上面找到的 IP 連接到 Linux 伺服器。

下圖顯示使用 Edge 瀏覽器連接到 node.js 伺服器的範例。

![從 Windows 存取 Linux 網路應用程式](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>從 Linux 存取 Windows 應用程式
若要存取 Windows 網路應用程式, 您必須使用主機電腦的 IP 位址。 您可以使用下列步驟來執行此動作:

- 執行命令`cat /etc/resolv.conf`並複製該字詞`nameserver`之後的 ip 位址, 以取得主機電腦的 ip 位址。 
- 使用複製的 IP 位址連接到任何 Windows 伺服器。


下圖顯示這種情況的範例，方式是連線到在 Windows 中執行的 node.js 伺服器 (透過 curl)。


![從 Windows 存取 Linux 網路應用程式](media/wsl2-network-l2w.png)

### <a name="other-networking-considerations"></a>其他網路功能考慮

使用遠端 IP 位址連線到您的應用程式時，系統會將其視為來自區域網路 (LAN) 的連線。這表示您必須確定您的應用程式可以接受 LAN 連線，也就是：您可能需要將您的應用程式繫結至 `0.0.0.0`，而不是 `127.0.0.1`。例如，在使用 flask 的 python 中，可以使用下列命令來完成此作業：`app.run(host='0.0.0.0')`。在進行這些變更時，請記住安全性，因為這會允許來自您 LAN 的連線。

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>瞭解 WSL 2 會使用 VHD, 以及當您達到其大小上限時該怎麼辦
WSL 2 會將您的所有 Linux 檔案儲存在使用 ext4 檔案系統的 VHD 內。此 VHD 會自動調整大小以符合您的儲存需求。此 VHD 也具有 256GB 的初始大小上限。如果您的發行版本大小成長為大於 256GB，您將會看到錯誤，說明您已用盡磁碟空間。您可以藉由擴充 VHD 大小來修正這些問題。有關如何執行此動作的指示如下：

1. 使用`wsl --shutdown`命令終止所有 WSL 實例
2. 尋找您的發行版本安裝套件名稱 'PackageFamilyName'
   - 在 powershell 提示字元 (其中 'distro' 是您的發行版本名稱) 中，請輸入:
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. 找出 WSL 2 安裝所使用的 VHD 檔案完整路徑，這會是您的 'pathToVHD'：
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 完成下列命令以調整您的 WSL 2 VHD 大小
   - 以系統管理員許可權開啟 [命令提示字元] 視窗, 然後執行下列命令:
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. 啟動您的 WSL 發行版本
6. 讓 WSL 知道它可以擴充其檔案系統的大小
   - 在您的 WSL 發行版本中執行下列命令:
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 複製此專案的名稱, 如下所示:/dev/sdXX (X 代表任何其他字元)
      - `sudo resize2fs /dev/sdXX`
         - 請務必使用您稍早複製的值, 您可能需要使用: `apt install resize2fs`。

請注意：一般來說，請不要使用 Windows 工具或編輯器修改、移動或存取位於 AppData 資料夾內的 WSL 相關檔案。這麼做可能會導致您的 Linux 發行版本損毀。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 會在啟動時使用一些記憶體
WSL 2 會在實際的 Linux 核心上使用輕量公用程式 VM, 以提供絕佳的檔案系統效能和完整的系統呼叫相容性, 同時仍能以 WSL 1 的速度快速、整合和回應。 此公用程式 VM 具有小型的記憶體使用量, 並會在啟動時配置虛擬位址支援的記憶體。 它會設定為從您總記憶體的一小部分開始。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>初次預覽組建中的跨 OS 檔案速度會較慢
從 Linux 應用程式存取 Windows 檔案, 或從 Windows 應用程式存取 Linux 檔案時, 您會發現相較于 WSL 1 的檔案速度比較慢。 這是 WSL 2 中架構變更的結果, 而 WSL 小組會主動調查如何改善這項體驗。
