---
title: Linux 使用者帳戶和權限
description: 使用者帳戶和權限管理適用於 Linux 的 Windows 子系統的參考。
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 使用者帳戶的 windows 子系統
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063596"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="fb97d-104">使用者帳戶和適用於 Linux 的 Windows 子系統的權限</span><span class="sxs-lookup"><span data-stu-id="fb97d-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="fb97d-105">建立您的 Linux 使用者是新的 Linux 散發套件在 WSL 上所設定的第一個步驟。</span><span class="sxs-lookup"><span data-stu-id="fb97d-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="fb97d-106">您所建立的第一個使用者帳戶會自動設定使用幾個特殊的屬性：</span><span class="sxs-lookup"><span data-stu-id="fb97d-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="fb97d-107">是您預設的使用者--它登入時自動啟動。</span><span class="sxs-lookup"><span data-stu-id="fb97d-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="fb97d-108">它是預設的 Linux 系統管理員 （sudo 群組的成員）。</span><span class="sxs-lookup"><span data-stu-id="fb97d-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="fb97d-109">適用於 Linux 的 Windows 子系統上執行的每個 Linux 散發套件都有自己的 Linux 使用者帳戶和密碼。</span><span class="sxs-lookup"><span data-stu-id="fb97d-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="fb97d-110">您必須設定的 Linux 使用者帳戶新增通訊群組、 重新安裝，或重設的任何時間。</span><span class="sxs-lookup"><span data-stu-id="fb97d-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="fb97d-111">Linux 使用者帳戶不是只有獨立每個散發，它們也是獨立於您的 Windows 使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="fb97d-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="fb97d-112">重設 Linux 密碼</span><span class="sxs-lookup"><span data-stu-id="fb97d-112">Resetting your Linux password</span></span>

<span data-ttu-id="fb97d-113">如果您可以存取您的 Linux 使用者帳戶，而且知道您目前的密碼，將它變更 linux 密碼重設工具，該分佈，最可能的`passwd`。</span><span class="sxs-lookup"><span data-stu-id="fb97d-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="fb97d-114">如果不是可行，根據散發套件，您可以藉由重設預設的使用者重設密碼。</span><span class="sxs-lookup"><span data-stu-id="fb97d-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="fb97d-115">WSL 會提供預設的使用者標記，來識別哪一個使用者帳戶自動登入，當您啟動 WSL。</span><span class="sxs-lookup"><span data-stu-id="fb97d-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="fb97d-116">由於許多散發套件包含根，也是以根使用者設定預設的使用者，且不需要密碼設定的命令，變更至根目錄的預設使用者是一個便利的工具，針對密碼重設等。</span><span class="sxs-lookup"><span data-stu-id="fb97d-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="fb97d-117">Creators Update 及更早版本</span><span class="sxs-lookup"><span data-stu-id="fb97d-117">For Creators Update and earlier</span></span>
<span data-ttu-id="fb97d-118">如果您執行 Windows 10 Creators update 或更早版本，您可以變更預設 Bash 使用者執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="fb97d-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="fb97d-119">變更預設使用者`root`:</span><span class="sxs-lookup"><span data-stu-id="fb97d-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="fb97d-120">執行`bash.exe`立即登入成`root`:</span><span class="sxs-lookup"><span data-stu-id="fb97d-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="fb97d-121">重設密碼使用散發套件的 密碼 命令，並關閉 Linux 主控台：</span><span class="sxs-lookup"><span data-stu-id="fb97d-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="fb97d-122">從 Windows CMD 重設為一般 Linux 使用者帳戶的預設使用者：</span><span class="sxs-lookup"><span data-stu-id="fb97d-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="fb97d-123">Fall Creators Update 和更新版本</span><span class="sxs-lookup"><span data-stu-id="fb97d-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="fb97d-124">若要查看哪些命令可供特定的分佈，請執行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="fb97d-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="fb97d-125">例如，使用 Ubuntu 安裝：</span><span class="sxs-lookup"><span data-stu-id="fb97d-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="fb97d-126">使用 Ubuntu 的逐步指示的步驟：</span><span class="sxs-lookup"><span data-stu-id="fb97d-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="fb97d-127">開啟 CMD</span><span class="sxs-lookup"><span data-stu-id="fb97d-127">Open CMD</span></span>
1. <span data-ttu-id="fb97d-128">若要設定預設的 Linux 使用者`root`:</span><span class="sxs-lookup"><span data-stu-id="fb97d-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="fb97d-129">啟動您的 Linux 散發套件 (`ubuntu`)。</span><span class="sxs-lookup"><span data-stu-id="fb97d-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="fb97d-130">您會自動登入為`root`:</span><span class="sxs-lookup"><span data-stu-id="fb97d-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="fb97d-131">重設您的密碼使用`passwd`命令：</span><span class="sxs-lookup"><span data-stu-id="fb97d-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="fb97d-132">從 Windows CMD 重設為一般 Linux 使用者帳戶的預設使用者。</span><span class="sxs-lookup"><span data-stu-id="fb97d-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="fb97d-133">Permissions</span><span class="sxs-lookup"><span data-stu-id="fb97d-133">Permissions</span></span>

<span data-ttu-id="fb97d-134">有兩個重要的概念，要牢記在心，就在 WSL 的權限：</span><span class="sxs-lookup"><span data-stu-id="fb97d-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="fb97d-135">Windows 權限模型會控管 Windows 資源的處理序的權限</span><span class="sxs-lookup"><span data-stu-id="fb97d-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="fb97d-136">Linux 的權限模型控制 Linux 資源的處理序的權限</span><span class="sxs-lookup"><span data-stu-id="fb97d-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="fb97d-137">當 Linux 在 WSL 上執行，Linux 會有相同的 Windows 權限，其啟動的程序。</span><span class="sxs-lookup"><span data-stu-id="fb97d-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="fb97d-138">可以在其中兩個權限等級中啟動 Linux:</span><span class="sxs-lookup"><span data-stu-id="fb97d-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="fb97d-139">一般 （非提高權限）：Linux 執行的登入的使用者權限</span><span class="sxs-lookup"><span data-stu-id="fb97d-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="fb97d-140">提高權限/系統管理：以提高權限/系統管理員的 Windows 權限執行的 Linux</span><span class="sxs-lookup"><span data-stu-id="fb97d-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="fb97d-141">因為，提高權限處理程序可以變更/損毀的全系統設定和資料，和可存取/修改受保護的檔案和資料夾，**避免**啟動提高程序，除非絕對需要的時候-不論它們是 Windows 或Linux 應用程式/tools/殼層 ！</span><span class="sxs-lookup"><span data-stu-id="fb97d-141">Because that elevated processes can change/damage system-wide settings and data, and can access/modify protected files and folders, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="fb97d-142">上述的 Windows 權限是獨立的中的 Linux 執行個體的權限：Linux 「 根權限 」 只會影響使用者的權限中的 Linux 環境與檔案系統;它們會將不會影響對授與 Windows 權限。</span><span class="sxs-lookup"><span data-stu-id="fb97d-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="fb97d-143">因此，以 root 身分執行 Linux 處理序 (例如，透過`sudo`) 只會處理在 Linux 環境中的系統管理員權限授與。</span><span class="sxs-lookup"><span data-stu-id="fb97d-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

**<span data-ttu-id="fb97d-144">範例：</span><span class="sxs-lookup"><span data-stu-id="fb97d-144">Example:</span></span>**    
<span data-ttu-id="fb97d-145">Windows 系統管理員權限的 Bash 工作階段可以存取`cd /mnt/c/Users/Administrator`沒有系統管理員權限就會看到 「 拒絕的權限 」 的錯誤時的 Bash 工作階段。</span><span class="sxs-lookup"><span data-stu-id="fb97d-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="fb97d-146">在 Linux 中，輸入`sudo cd /mnt/c/Users/Administrator`由於 Windows 內的權限由 Windows，將會授與系統管理員的目錄的存取權。</span><span class="sxs-lookup"><span data-stu-id="fb97d-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="fb97d-147">Linux 的權限模型是很重要時，使用者已根據目前的 Linux 使用者的權限的 Linux 環境內。</span><span class="sxs-lookup"><span data-stu-id="fb97d-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

**<span data-ttu-id="fb97d-148">範例：</span><span class="sxs-lookup"><span data-stu-id="fb97d-148">Example:</span></span>**  
<span data-ttu-id="fb97d-149">Sudo 群組中的使用者可以執行`sudo apt update`。</span><span class="sxs-lookup"><span data-stu-id="fb97d-149">A user in the sudo group may run `sudo apt update`.</span></span>
