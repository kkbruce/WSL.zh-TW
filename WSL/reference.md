---
title: 如需 Linux 命令參考的 Windows 子系統
description: 管理適用於 Linux 的 Windows 子系統的命令清單
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu 的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063576"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>適用於 Linux 的 Windows 子系統的命令參考

> `lxrun.exe` 已被取代，自 Windows 10 1803年和更新版本。

此命令`lxrun.exe`可以用來與互動[Windows for Linux 子系統 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接。  這些命令會安裝到`\Windows\System32`目錄並可能在 Windows 命令提示字元中，或在 PowerShell 中執行。

* `lxrun.exe` 用來管理 WSL。  此命令可以用來安裝或解除安裝的 Ubuntu 映像中。


| 命令                     | 描述                     |
|:----------------------------|:---------------------------|
| `bash`                      | 會啟動目前的目錄中的 Bash 殼層。  如果未自動安裝 Bash 殼層中執行 `lxrun /install` |
| `bash ~`                    | 啟動到主目錄中使用者的 Ubuntu 的 bash 殼層。  類似於執行 cd ~            |
| `bash -c "<command>"`       | 執行命令，將輸出列印並結束回到 Windows 命令提示字元。 <br/> <br/> 範例： **bash-c"ls"** |

<p>

| 命令                     | 描述                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 命令用來管理 WSL 執行個體。 |
| `lxrun /install`            | 開始下載與安裝程序。 <br/> **/y**可能會加入至略過所有提示。  會自動接受確認提示，而且預設使用者設定為根。          |
| `lxrun /uninstall`          | 解除安裝，並刪除 Ubuntu 映像。  依預設這不會移除使用者的 Ubuntu 主目錄。 <br/> **/y**可能加入自動接受確認提示 <br/>**完整/** 解除安裝，並刪除使用者的 Ubuntu 主目錄         |
| `lxrun /setdefaultuser <userName>`     | Ubuntu 使用者設定預設 Bash。 如果指定的使用者不存在，會提示輸入密碼。  如需詳細資訊，請造訪： https://aka.ms/wslusers。 <br/> **/y**許可 promping 的密碼。  不需要密碼，就會建立使用者。|
| `lxrun /update`            | 更新的子系統套件索引          |
