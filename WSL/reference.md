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
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="3ee57-104">適用於 Linux 的 Windows 子系統的命令參考</span><span class="sxs-lookup"><span data-stu-id="3ee57-104">Command Reference for Windows Subsystem for Linux</span></span>

> <span data-ttu-id="3ee57-105">`lxrun.exe` 已被取代，自 Windows 10 1803年和更新版本。</span><span class="sxs-lookup"><span data-stu-id="3ee57-105">`lxrun.exe` is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="3ee57-106">此命令`lxrun.exe`可以用來與互動[Windows for Linux 子系統 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接。</span><span class="sxs-lookup"><span data-stu-id="3ee57-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="3ee57-107">這些命令會安裝到`\Windows\System32`目錄並可能在 Windows 命令提示字元中，或在 PowerShell 中執行。</span><span class="sxs-lookup"><span data-stu-id="3ee57-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* <span data-ttu-id="3ee57-108">`lxrun.exe` 用來管理 WSL。</span><span class="sxs-lookup"><span data-stu-id="3ee57-108">`lxrun.exe` is used to manage WSL.</span></span>  <span data-ttu-id="3ee57-109">此命令可以用來安裝或解除安裝的 Ubuntu 映像中。</span><span class="sxs-lookup"><span data-stu-id="3ee57-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="3ee57-110">命令</span><span class="sxs-lookup"><span data-stu-id="3ee57-110">Command</span></span>                     | <span data-ttu-id="3ee57-111">描述</span><span class="sxs-lookup"><span data-stu-id="3ee57-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="3ee57-112">會啟動目前的目錄中的 Bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="3ee57-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="3ee57-113">如果未自動安裝 Bash 殼層中執行 `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="3ee57-113">If the Bash shell is not installed automatically runs `lxrun /install`</span></span> |
| `bash ~`                    | <span data-ttu-id="3ee57-114">啟動到主目錄中使用者的 Ubuntu 的 bash 殼層。</span><span class="sxs-lookup"><span data-stu-id="3ee57-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="3ee57-115">類似於執行 cd ~</span><span class="sxs-lookup"><span data-stu-id="3ee57-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="3ee57-116">執行命令，將輸出列印並結束回到 Windows 命令提示字元。</span><span class="sxs-lookup"><span data-stu-id="3ee57-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="3ee57-117">範例： **bash-c"ls"**</span><span class="sxs-lookup"><span data-stu-id="3ee57-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="3ee57-118">命令</span><span class="sxs-lookup"><span data-stu-id="3ee57-118">Command</span></span>                     | <span data-ttu-id="3ee57-119">描述</span><span class="sxs-lookup"><span data-stu-id="3ee57-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="3ee57-120">Lxrun 命令用來管理 WSL 執行個體。</span><span class="sxs-lookup"><span data-stu-id="3ee57-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="3ee57-121">開始下載與安裝程序。</span><span class="sxs-lookup"><span data-stu-id="3ee57-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="3ee57-122">**/y**可能會加入至略過所有提示。</span><span class="sxs-lookup"><span data-stu-id="3ee57-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="3ee57-123">會自動接受確認提示，而且預設使用者設定為根。</span><span class="sxs-lookup"><span data-stu-id="3ee57-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="3ee57-124">解除安裝，並刪除 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="3ee57-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="3ee57-125">依預設這不會移除使用者的 Ubuntu 主目錄。</span><span class="sxs-lookup"><span data-stu-id="3ee57-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="3ee57-126">**/y**可能加入自動接受確認提示</span><span class="sxs-lookup"><span data-stu-id="3ee57-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="3ee57-127">**完整/** 解除安裝，並刪除使用者的 Ubuntu 主目錄</span><span class="sxs-lookup"><span data-stu-id="3ee57-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="3ee57-128">Ubuntu 使用者設定預設 Bash。</span><span class="sxs-lookup"><span data-stu-id="3ee57-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="3ee57-129">如果指定的使用者不存在，會提示輸入密碼。</span><span class="sxs-lookup"><span data-stu-id="3ee57-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="3ee57-130">如需詳細資訊，請造訪： https://aka.ms/wslusers。</span><span class="sxs-lookup"><span data-stu-id="3ee57-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="3ee57-131">**/y**許可 promping 的密碼。</span><span class="sxs-lookup"><span data-stu-id="3ee57-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="3ee57-132">不需要密碼，就會建立使用者。</span><span class="sxs-lookup"><span data-stu-id="3ee57-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="3ee57-133">更新的子系統套件索引</span><span class="sxs-lookup"><span data-stu-id="3ee57-133">Updates the subsystem's package index</span></span>          |
