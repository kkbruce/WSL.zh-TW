---
title: 疑難排解適用於 Linux 的 Windows Susbystem
description: 提供常見錯誤的詳細的資訊，並發出人遇到同時適用於 Linux 的 Windows Susbystem 上執行 Linux。
keywords: BashOnWindows，bash，wsl、 windows、 windowssubsystem、 ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: feb9e25da73eeb0d7f0cef4014221a42e2ca179b
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040851"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>疑難排解適用於 Linux 的 Windows 子系統

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash 失去網路連線一次連線到 VPN

如果連接到在 Windows 上的 VPN 之後，bash 會失去網路連線，請嘗試從這個解決方法，在 bash 中。 此因應措施可讓您以手動方式覆寫透過 DNS 解析`/etc/resolv.conf`。

1. 請記下的 vpn，如此一來從 DNS 伺服器 `ipconfig.exe /all`
2. 建立一份現有 resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 取消連結目前 resolv.con `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 開啟`/etc/resolv.conf`和 <br/>
   a. 刪除的第一行，從檔案，指出 「\#這個檔案自動產生的 WSL。 若要停止自動產生這個檔案，移除這行文字。 」。 <br/>
   b. 新增 DNS 項目 (1) 從上方為 DNS 伺服器清單中的第一個項目。 <br/>
   c. 關閉檔案。 <br/>

一旦您已經中斷連線 VPN，您就必須還原所做的變更`/etc/resolv.conf`。 若要這樣做，請執行：
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>啟動 WSL 或安裝發佈傳回錯誤碼

請遵循[這些指示](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)收集詳細的記錄，並在我們的 GitHub 上提出問題。

### <a name="updating-bash-on-ubuntu-on-windows"></a>在 Windows 上 Ubuntu 之 Bash 上的更新

有可能需要更新的 Windows 上 Ubuntu 之 Bash 上的兩個元件。 

1. 適用於 Linux 的 Windows 子系統
  
   升級在 Windows 上 Ubuntu 之 Bash 上的這個部分可讓在任何新的修正外框輪廓[版本資訊](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)。 請確定您已訂閱 Windows Insider 計劃，而且是最新的組建。 包括重設您的 Ubuntu 更精細的幅度控制執行個體，請參閱[命令參考頁面](https://msdn.microsoft.com/en-us/commandline/wsl/reference)。

2. Ubuntu 使用者二進位檔 

   升級在 Windows 上 Ubuntu 之 Bash 上的這個部分，將 Ubuntu 使用者二進位檔，包括您已透過 apt-get 安裝的應用程式安裝任何更新。 若要更新執行下列命令在 Bash 中：
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt get 升級錯誤
有些套件會使用我們尚未在尚未實作的功能。 `udev`比方說，尚未支援，而導致幾`apt-get upgrade`錯誤。

若要修正的相關問題`udev`，請遵循下列步驟：

1. 寫入下列命令以`/usr/sbin/policy-rc.d`並儲存變更。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 新增執行權限 `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 執行下列命令
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"Error:0x80040306 」 上安裝
這必須與事實，我們不支援舊版的主控台。
若要關閉舊版主控台：

1. 開啟 cmd.exe
1. 以滑鼠右鍵按一下標題列-> 屬性-> 取消核取 使用舊版主控台
1. 按一下 [確定]

### <a name="error-0x80040154-after-windows-update"></a>"Error:0x80040154 」 Windows 更新之後
針對 Linux 功能的 Windows 子系統可能會停用在 Windows 的更新。 如果發生這種情況則必須重新啟用 Windows 功能。 啟用 Windows 子系統中，可以找到 Linux 的指示[安裝指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

### <a name="changing-the-display-language"></a>變更顯示語言
WSL 安裝將會嘗試自動變更以符合您的 Windows 安裝的地區設定的 Ubuntu 地區設定。  如果不想讓此行為，您可以執行這個命令來安裝完成之後，變更 Ubuntu 地區設定。  您必須重新啟動 bash.exe 這項變更才會生效。

下列範例會變更為 EN-US 地區設定：
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 系統還原之後的安裝問題
1.  刪除`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`資料夾。 <br/>
  **注意：請不要這樣如果選擇性的功能已完整安裝和使用。**
2.  啟用 WSL 選用功能 （如果尚未）
3.  重新開機
4.  lxrun / 解除安裝/完整
5.  安裝 bash

### <a name="no-internet-access-in-wsl"></a>在 WSL 沒有網際網路存取權
某些使用者有特定的防火牆應用程式封鎖網際網路存取，在 WSL 使用回報的問題。  報告在防火牆︰

1. Kaspersky
1. AVG
1. 太好了

在某些情況下關閉防火牆可供存取。  在某些情況下單純地安裝防火牆會封鎖其存取權。

### <a name="permission-denied-error-when-using-ping"></a>使用 ping 時的權限遭拒錯誤
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[年度更新版](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

在 Windows 中的系統管理員權限，才能在 WSL 執行 ping。  若要執行 ping，身為管理員，Windows 上，執行 ubuntu 的 Bash 或 bash.exe 從執行系統管理員權限的 CMD/PowerShell 提示字元。

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[建置 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  不再需要系統管理員權限。

### <a name="bash-is-hung"></a>Bash 已停止
如果同時使用 bash，您會發現該 bash 是停止 （或發生死結） 和未回應的輸入，協助我們診斷問題所收集和報告的記憶體傾印。 請注意下列步驟將會損毀您的系統。 請不要這樣如果您不熟悉，或儲存您的工作之前執行此動作。  <br/>
若要收集記憶體傾印：
1. 將記憶體傾印類型變更為 「 完整記憶體傾印 」。 而變更的傾印型別，記下您目前的類型。
2. 使用[步驟](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)設定損毀使用鍵盤來控制。
3. 重現的停止回應或死結。
4. 損毀系統使用的索引鍵的順序，從 (2)。
5. 系統將會損毀，並收集記憶體傾印。
6. 一旦在系統重新開機，回報至 memory.dmp secure@microsoft.com。 傾印檔案的預設位置是 %SystemRoot%\memory.dmp 或 C:\Windows\memory.dmp，如果 c： 系統磁碟機。 在 電子郵件，請注意，傾印 WSL 或 Bash on Windows 小組。
7. 還原為原始設定的記憶體傾印類型。

### <a name="check-your-build-number"></a>檢查您的組建編號

若要尋找您的電腦架構和 Windows 組建編號，請開啟  
**設定** > **系統** > **相關**

尋求**作業系統組建**並**系統類型**欄位。  
    ![建立螢幕擷取畫面和系統類型的欄位](media/system.png) 


若要尋找您的 Windows Server 組建編號，請在 PowerShell 中執行下列：  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>確認已啟用 WSL
您可以確認適用於 Linux 的 Windows 子系統，會啟用在 PowerShell 中執行下列命令：  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH 伺服器連線問題
嘗試將 SSH 伺服器連接會失敗，發生下列錯誤："127.0.0.1 關閉的連接埠 22，"。
1. 請確定您的 OpenSSH 伺服器正在執行：
   ``` BASH
   sudo service ssh status
   ```
   然後，您已遵循本教學課程： https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. 停止 sshd 服務，並在偵錯模式下啟動 sshd:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 檢查啟動記錄檔，並確定 HostKeys 可用，而且您沒有看到記錄檔訊息，例如：
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

如果您看到這類訊息，而且索引鍵為下方遺漏`/etc/ssh/`，您必須重新產生金鑰，或只是清除並安裝 openssh 伺服器：
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

