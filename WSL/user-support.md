---
title: Linux 使用者帳戶和許可權
description: 適用于 Linux 的 Windows 子系統的使用者帳戶和版權管理的參考。
keywords: BashOnWindows、bash、wsl、windows、適用于 linux 的 windows 子系統、windowssubsystem、ubuntu、使用者帳戶
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 0d00b43d059e72edd4e2a5b9591c29441f461fca
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040830"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="28414-104">適用于 Linux 的 Windows 子系統的使用者帳戶和許可權</span><span class="sxs-lookup"><span data-stu-id="28414-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="28414-105">建立 Linux 使用者是在 WSL 上設定新的 Linux 散發套件的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="28414-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="28414-106">您所建立的第一個使用者帳戶會自動設定一些特殊屬性:</span><span class="sxs-lookup"><span data-stu-id="28414-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="28414-107">這是您的預設使用者--它會在啟動時自動登入。</span><span class="sxs-lookup"><span data-stu-id="28414-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="28414-108">預設為 Linux 系統管理員 (sudo 群組的成員)。</span><span class="sxs-lookup"><span data-stu-id="28414-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="28414-109">在適用于 Linux 的 Windows 子系統上執行的每個 Linux 散發套件都有自己的 Linux 使用者帳戶和密碼。</span><span class="sxs-lookup"><span data-stu-id="28414-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="28414-110">每當您新增散發、重新安裝或重設時, 都必須設定 Linux 使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="28414-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="28414-111">Linux 使用者帳戶不只是每個散發套件都獨立, 它們也獨立于您的 Windows 使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="28414-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="28414-112">重設您的 Linux 密碼</span><span class="sxs-lookup"><span data-stu-id="28414-112">Resetting your Linux password</span></span>

<span data-ttu-id="28414-113">如果您有 Linux 使用者帳戶的存取權, 並知道目前的密碼, 請使用該發佈的 Linux 密碼重設工具加以變更- `passwd`-最有可能。</span><span class="sxs-lookup"><span data-stu-id="28414-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="28414-114">如果這不是選項, 則視散發套件而定, 您可以藉由重設預設使用者來重設密碼。</span><span class="sxs-lookup"><span data-stu-id="28414-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="28414-115">WSL 提供預設的使用者標記, 以識別當您啟動 WSL 時, 會自動登入的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="28414-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="28414-116">由於許多發行版本都包含將預設使用者設定為 root 的命令, 以及未設定密碼的根使用者, 因此將預設使用者變更為 root 是很方便的工具, 可用於重設密碼等。</span><span class="sxs-lookup"><span data-stu-id="28414-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="28414-117">適用于建立者更新和更早版本</span><span class="sxs-lookup"><span data-stu-id="28414-117">For Creators Update and earlier</span></span>
<span data-ttu-id="28414-118">如果您執行的是 Windows 10 建立者更新或更早的版本, 您可以執行下列命令來變更預設 Bash 使用者:</span><span class="sxs-lookup"><span data-stu-id="28414-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="28414-119">將預設使用者變更為`root`:</span><span class="sxs-lookup"><span data-stu-id="28414-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="28414-120">執行`bash.exe`以立即`root`登入:</span><span class="sxs-lookup"><span data-stu-id="28414-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="28414-121">使用發佈的密碼命令重設您的密碼, 然後關閉 Linux 主控台:</span><span class="sxs-lookup"><span data-stu-id="28414-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="28414-122">從 Windows CMD, 將您的預設使用者重設回一般的 Linux 使用者帳戶:</span><span class="sxs-lookup"><span data-stu-id="28414-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="28414-123">適用于秋季建立者更新和更新版本</span><span class="sxs-lookup"><span data-stu-id="28414-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="28414-124">若要查看哪些命令可用於特定的散發, 請`[distro.exe] /?`執行。</span><span class="sxs-lookup"><span data-stu-id="28414-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="28414-125">例如, 已安裝 Ubuntu:</span><span class="sxs-lookup"><span data-stu-id="28414-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="28414-126">使用 Ubuntu 的逐步指示:</span><span class="sxs-lookup"><span data-stu-id="28414-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="28414-127">開啟 CMD</span><span class="sxs-lookup"><span data-stu-id="28414-127">Open CMD</span></span>
1. <span data-ttu-id="28414-128">將預設的 Linux 使用者設定`root`為:</span><span class="sxs-lookup"><span data-stu-id="28414-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="28414-129">啟動您的 Linux 散發`ubuntu`套件 ()。</span><span class="sxs-lookup"><span data-stu-id="28414-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="28414-130">您將會自動登`root`入為:</span><span class="sxs-lookup"><span data-stu-id="28414-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="28414-131">使用命令重設您`passwd`的密碼:</span><span class="sxs-lookup"><span data-stu-id="28414-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="28414-132">從 Windows CMD, 將您的預設使用者重設回一般的 Linux 使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="28414-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="28414-133">Permissions</span><span class="sxs-lookup"><span data-stu-id="28414-133">Permissions</span></span>

<span data-ttu-id="28414-134">在 WSL 中的許可權時, 有兩個重要的概念要謹記在心:</span><span class="sxs-lookup"><span data-stu-id="28414-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="28414-135">Windows 許可權模型可控制處理常式對 Windows 資源的許可權</span><span class="sxs-lookup"><span data-stu-id="28414-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="28414-136">Linux 許可權模型可控制處理常式對 Linux 資源的許可權</span><span class="sxs-lookup"><span data-stu-id="28414-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="28414-137">在 WSL 上執行 Linux 時, Linux 的 Windows 許可權會與啟動它的進程相同。</span><span class="sxs-lookup"><span data-stu-id="28414-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="28414-138">您可以在下列兩種許可權層級之一啟動 Linux:</span><span class="sxs-lookup"><span data-stu-id="28414-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="28414-139">一般 (未提高許可權):Linux 會以已登入使用者的許可權執行</span><span class="sxs-lookup"><span data-stu-id="28414-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="28414-140">提高許可權/系統管理員:使用提高許可權/管理 Windows 許可權執行 Linux</span><span class="sxs-lookup"><span data-stu-id="28414-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="28414-141">因為提高許可權的進程可以存取/修改 (因而損毀) 全系統的設定和全系統/受保護的資料, 除非您絕對需要, 否則請**避免**啟動提高許可權的進程 (不論它們是 Windows 或 Linux 應用程式/工具/)殼層!</span><span class="sxs-lookup"><span data-stu-id="28414-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="28414-142">上述 Windows 許可權與 Linux 實例內的許可權無關:Linux 「根許可權」只會影響使用者在 Linux 環境中的許可權, & filesystem;它們不會影響授與的 Windows 許可權。</span><span class="sxs-lookup"><span data-stu-id="28414-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="28414-143">因此, 以 root 身分執行 Linux 進程 (例如 via `sudo`) 只會授與該進程在 Linux 環境中的系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="28414-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="28414-144">**範例：**   </span><span class="sxs-lookup"><span data-stu-id="28414-144">**Example:**  </span></span>  
<span data-ttu-id="28414-145">具有 Windows 管理員許可權的 bash 會話可能會`cd /mnt/c/Users/Administrator`存取, 而沒有系統管理員許可權的 bash 會話會看到「許可權被拒」錯誤。</span><span class="sxs-lookup"><span data-stu-id="28414-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="28414-146">在 Linux 中, `sudo cd /mnt/c/Users/Administrator`因為 windows 中的許可權是由 windows 所管理, 所以輸入不會授與系統管理員目錄的存取權。</span><span class="sxs-lookup"><span data-stu-id="28414-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="28414-147">在 Linux 環境中, 如果使用者有以目前的 Linux 使用者為基礎的許可權, Linux 許可權模型就很重要。</span><span class="sxs-lookup"><span data-stu-id="28414-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="28414-148">**範例:**</span><span class="sxs-lookup"><span data-stu-id="28414-148">**Example:**</span></span>  
<span data-ttu-id="28414-149">Sudo 群組中的使用者可能會執行`sudo apt update`。</span><span class="sxs-lookup"><span data-stu-id="28414-149">A user in the sudo group may run `sudo apt update`.</span></span>
