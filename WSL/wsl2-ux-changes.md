---
title: UX WSL 1 」 與 「 WSL 2 之間的變更
description: WSL 1 和 WSL 2 之間的使用者體驗變更
keywords: BashOnWindows、 bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038098"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 和 WSL 2 之間的使用者體驗變更

此頁面會透過使用者體驗和之間的差異 WSL 1 WSL 2 預覽。 要注意的主要變更是：

- 放置您的 Linux 應用程式會存取 Linux 根檔案系統的效能速度檔案中的檔案
- 在 WSL 2 預覽的初始組建中，您將需要存取網路應用程式使用的 IP 位址與不使用 localhost

而以下是您可能會發現其他變更的完整清單：

- WSL 2 使用 VHD 來儲存您的檔案，而且如果您達到其大小上限您可能需要將它展開
- 啟動時，WSL 2 現在會使用記憶體的一小部分
- 跨 OS 檔案存取速度將會在初始的預覽版組建變慢

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>將您的 Linux 檔案放在您的 Linux 根檔案系統
請務必將您的 Linux 將經常存取的檔案放在您的 Linux 內的應用程式根目錄檔案系統，才能享有檔案效能優勢。 這些檔案一定要在 Linux 根檔案系統，以更快速的檔案系統存取。 我們也已可將 Windows 應用程式存取 Linux 根檔案系統 （例如檔案總管 中 ！ 請嘗試執行：`explorer.exe /`中您 bash 殼層並查看) 這麼做會讓這項轉換更加方便。 

## <a name="accessing-network-applications"></a>存取網路的應用程式
在 WSL 2 預覽的初始組建，您必須從 Windows 使用您的 Linux 散發版本，並從 Linux 使用主機電腦的 IP 位址的任何 Windows 伺服器的 IP 位址存取的任何 Linux 伺服器。 這是暫時性的且若要修正我們的優先順序清單上非常高的項目。

### <a name="accessing-linux-applications-from-windows"></a>從 Windows 存取 Linux 應用程式
如果您有伺服器在 WSL 散發版本，表示您要尋找加強您的散發版本的虛擬機器的 IP 位址，並使用該 IP 位址連線到它。 您可以依照下列步驟來這麼做：

- 執行命令來取得您的散發版本的 IP 位址`ip addr`內 WSL distro 並尋找下加以`inet`的值`eth0`介面。
   - 您可以找到此更輕鬆地篩選使用 grep 命令的輸出如下： `ip addr | grep eth0`。
- 連接到您在上面找到您 Linux 伺服器使用的 IP。

下圖顯示這個範例藉由連接到使用 microsoft Edge 瀏覽器的 nodeJS 伺服器。

![從 Windows 存取 Linux 的網路應用程式](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>從 Linux 存取 Windows 應用程式
若要存取 Windows 網路應用程式，您必須使用主機電腦的 IP 位址。 您可以執行下列步驟：

- 執行命令來取得您的主機電腦的 IP 位址`cat /etc/resolv.conf`並複製下列詞彙的 IP 位址`nameserver`。 
- 連線至任何使用複製的 IP 位址的 Windows 伺服器。

下圖顯示這個範例藉由連線到透過 curl 在 Windows 中執行的 python 伺服器。 

![從 Windows 存取 Linux 的網路應用程式](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>了解 WSL 2 使用 VHD，而如果您達到其大小上限，該怎麼辦
WSL 2 會儲存您所有的 Linux 檔案內使用 ext4 檔案系統的 VHD。 此 VHD 自動調整大小以符合您的儲存體需求。 此 VHD 也具有初始大小上限為 256 GB。 如果您的散發版本成長的大小必須大於 256 GB，您會看到錯誤指出您已用盡磁碟空間。 您可以修正這些方法是展開的 VHD 大小。 有關如何執行這項操作的指示如下：

1. 終止所有 WSL 執行個體使用`wsl --shutdown`命令
2. 完成下列命令來調整大小 WSL 2 VHD
   - 以系統管理員權限開啟命令提示字元 視窗，然後執行下列命令：
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. 啟動您的 WSL 散發套件
4. 請注意，它可以展開其檔案系統的大小 WSL
   - 在 WSL distro 中，執行下列命令：
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 複製此項目，看起來就像的名稱: / sdXX (具有 X 表示任何其他字元)
      - `sudo resize2fs /dev/sdXX`
         - 請確定使用的值之前，複製，而且您可能需要使用： `apt install resize2fs`。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 會使用一些記憶體，在啟動
WSL 2 會使用輕量級的公用程式 VM 上實際的 Linux 核心提供絕佳的檔案系統的效能和完整的系統呼叫仍正在執行時的相容性，就如同光線，快速、 整合和回應以 WSL 1。 此公用程式 VM 會具有較小的記憶體耗用量，並將備份的虛擬位址上配置的記憶體啟動。 它會設定為啟動與您的總記憶體的一小部分。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>跨作業系統檔案的速度將會在初始的預覽版組建變慢
您會發現檔案上的速度比 WSL 1 時從 Linux 應用程式，或從 Windows 應用程式存取 Linux 檔案存取 Windows 檔案。 這是在 WSL 2 的架構變更的結果，是指 WSL 小組正在調查上如何改善這項體驗。