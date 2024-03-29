---
title: 針對適用于 Linux 的 Windows 子系統進行疑難排解
description: 提供在適用于 Linux 的 Windows 子系統上執行 Linux 時, 常見錯誤和使用者遇到之問題的詳細資訊。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: 0c84fb710eca1b0ffabe437f98d5c17edbd6ea39
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307641"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>適用于 Linux 的 Windows 子系統疑難排解

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash 連接到 VPN 之後, 會失去網路連線能力

如果在連接到 Windows 上的 VPN 之後, bash 會失去網路連線, 請從 bash 內嘗試這個因應措施。 這個因應措施可讓您透過`/etc/resolv.conf`手動覆寫 DNS 解析。

1. 記下 VPN 的 DNS 伺服器, 使其無法執行`ipconfig.exe /all`
2. 建立現有 resolv.conf 的複本`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 取消連結目前的 resolv.conf`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 開啟`/etc/resolv.conf`和 <br/>
   a. 刪除檔案中的第一行, 這會顯示\# 「此檔案由 WSL 自動產生。 若要停止自動產生此檔案, 請移除這一行。」。 <br/>
   b. 將上述 (1) 中的 DNS 專案新增為 DNS 伺服器清單中的第一個專案。 <br/>
   c. 關閉檔案。 <br/>

當您中斷連線 VPN 之後, 您必須將變更還原到`/etc/resolv.conf`。 若要這麼做, 請執行:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>啟動 WSL 或安裝散發會傳回錯誤代碼

請遵循[這些指示](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)來收集詳細記錄, 並在我們的 GitHub 上提出問題。

### <a name="updating-bash-on-ubuntu-on-windows"></a>更新 Windows 上 Ubuntu 上的 Bash

Windows 上的 Ubuntu 有兩個可能需要更新的元件。 

1. 適用于 Linux 的 Windows 子系統
  
   在 Windows 上的 Ubuntu 上升級 Bash 的這個部分, 將會啟用[版本](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)資訊中的任何新修正程式概述。 請確定您已訂閱 Windows 測試人員方案, 且您的組建是最新的。 如需更精細的控制, 包括重設您的 Ubuntu 實例, 請參閱[命令參考頁面](https://msdn.microsoft.com/en-us/commandline/wsl/reference)。

2. Ubuntu 使用者二進位檔 

   在 Windows 上的 Ubuntu 上升級此部分的 Bash, 將會安裝 Ubuntu 使用者二進位檔的任何更新, 包括您透過 apt-get 所安裝的應用程式。 若要更新, 請在 Bash 中執行下列命令:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-取得升級錯誤
有些套件會使用我們尚未實行的功能。 `udev`例如, 尚不支援, 而且會導致數`apt-get upgrade`個錯誤。

若要修正與相關`udev`的問題, 請遵循下列步驟:

1. 將下列`/usr/sbin/policy-rc.d`程式寫入並儲存您的變更。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 將執行許可權新增至`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 執行下列命令
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error:0x80040306 "安裝時
這與我們不支援舊版主控台的事實有關。
若要關閉舊版主控台:

1. 開啟 cmd.exe
1. 以滑鼠右鍵按一下標題列-> 屬性-> 取消核取 [使用舊版主控台]
1. 按一下 [確定]

### <a name="error-0x80040154-after-windows-update"></a>"Error:0x80040154 "Windows update 之後
適用于 Linux 的 Windows 子系統功能可能會在 Windows 更新期間停用。 如果發生這種情況, 則必須重新啟用 Windows 功能。 如需如何啟用適用于 Linux 的 Windows 子系統的指示, 請參閱[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

### <a name="changing-the-display-language"></a>變更顯示語言
WSL install 會嘗試自動變更 Ubuntu 地區設定, 以符合 Windows 安裝的地區設定。  如果您不想要此行為, 您可以執行此命令, 以在安裝完成後變更 Ubuntu 地區設定。  您必須重新開機 bash, 這種變更才會生效。

下列範例會將地區設定變更為 en-us:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 系統還原後的安裝問題
1.  `%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`刪除資料夾。 <br/>
  **注意：如果您的選用功能已完整安裝且正常運作, 請不要這麼做。**
2.  啟用 WSL 選用功能 (如果尚未這麼做)
3.  重新開機
4.  lxrun/uninstall/full
5.  安裝 bash

### <a name="no-internet-access-in-wsl"></a>WSL 中沒有網際網路存取
某些使用者回報了在 WSL 中封鎖網際網路存取的特定防火牆應用程式問題。  回報的防火牆如下:

1. Kaspersky
1. AVG
1. Avast

在某些情況下, 關閉防火牆可讓您存取。  在某些情況下, 只安裝防火牆會顯示封鎖存取。

### <a name="permission-denied-error-when-using-ping"></a>使用 ping 時發生許可權拒絕錯誤
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[年度更新](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

需要 Windows 中的系統管理員許可權, 才能在 WSL 中執行 ping。  若要執行 ping, 請以系統管理員身分在 Windows 上的 Ubuntu 上執行 Bash, 或從具有系統管理員許可權的 CMD/PowerShell 提示字元執行 bash。

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[組建 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  不再需要系統管理員許可權。

### <a name="bash-is-hung"></a>Bash 已停止回應
當您使用 bash 時, 您會發現 bash 已停止回應 (或鎖死), 而且沒有回應輸入, 請收集和報告記憶體傾印, 以協助我們診斷問題。 請注意, 這些步驟將會損毀您的系統。 如果您不熟悉該作業, 或在執行此動作之前儲存您的工作, 請不要這麼做。  <br/>
若要收集記憶體傾印:
1. 將記憶體傾印類型變更為「完成記憶體傾印」。 變更傾印類型時, 請記下您目前的類型。
2. 使用 [使用鍵盤控制項設定當機] 的[步驟](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)。
3. 重現停止回應或鎖死。
4. 使用 (2) 中的機碼序列來損毀系統。
5. 系統會損毀並收集記憶體傾印。
6. 系統重新開機之後, 請將記憶體 dmp 回報給secure@microsoft.com。 傾印檔案的預設位置是%SystemRoot%\memory.dmp 或 C:\Windows\memory.dmp (如果 C: 是系統磁片磁碟機)。 在電子郵件中, 請注意, 傾印適用于 Windows 小組的 WSL 或 Bash。
7. 將記憶體傾印類型還原為原始設定。

### <a name="check-your-build-number"></a>檢查您的組建編號

若要尋找您電腦的架構和 Windows 組建編號, 請開啟  
**設定** > **系統**關於 > 

尋找 [**作業系統組建**] 和 [**系統類型**] 欄位。  
    ![[組建] 和 [系統類型] 欄位的螢幕擷取畫面](media/system.png) 


若要尋找您的 Windows Server 組建編號, 請在 PowerShell 中執行下列程式碼:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>確認已啟用 WSL
您可以在 PowerShell 中執行下列程式, 確認已啟用適用于 Linux 的 Windows 子系統:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH-伺服器連接問題
嘗試連接 SSH 伺服器失敗, 發生下列錯誤:「連接已由127.0.0.1 埠22關閉」。
1. 請確定您的 OpenSSH 伺服器正在執行:
   ``` BASH
   sudo service ssh status
   ```
   您已遵循此教學課程: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. 停止 sshd 服務並以 debug 模式啟動 sshd:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 檢查開機記錄, 並確認 HostKeys 可供使用, 而且您看不到記錄訊息, 例如:
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

如果您看到這類訊息, 而`/etc/ssh/`中遺漏了金鑰, 您就必須重新產生金鑰, 或只是清除 & 安裝 openssh-伺服器:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

