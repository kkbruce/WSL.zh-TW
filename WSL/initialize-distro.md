---
title: 初始化新的 WSL Linux 散發版本
description: 安裝適用于 WSL 的 Linux 散發版本之後, 請遵循下列簡單步驟來完成初始化
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499293"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="18dfe-104">將新安裝的散發版本初始化</span><span class="sxs-lookup"><span data-stu-id="18dfe-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="18dfe-105">下載並安裝散發版本之後, 您必須完成新散發版本的初始化:</span><span class="sxs-lookup"><span data-stu-id="18dfe-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="18dfe-106">啟動散發版本</span><span class="sxs-lookup"><span data-stu-id="18dfe-106">Launch a distro</span></span>
<span data-ttu-id="18dfe-107">若要完成新安裝散發版本的初始化, 請啟動新的實例。</span><span class="sxs-lookup"><span data-stu-id="18dfe-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="18dfe-108">若要這麼做, 您可以按一下 Microsoft Store 應用程式中的 [啟動] 按鈕, 或從 [開始] 功能表啟動散發版本:</span><span class="sxs-lookup"><span data-stu-id="18dfe-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="18dfe-109">秘訣：您可能想要將最常使用的散發版本釘選到 [開始] 功能表和/或您的工作列!</span><span class="sxs-lookup"><span data-stu-id="18dfe-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![從 [開始] 功能表啟動散發版本](media/start-menu.png)

> <span data-ttu-id="18dfe-111">在 Windows Server 上, 您可以從散發版本安裝資料夾啟動`<distro>.exe`散發版本的啟動器可執行檔。</span><span class="sxs-lookup"><span data-stu-id="18dfe-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="18dfe-112">第一次執行新安裝的散發版本時, 主控台視窗將會開啟, 而且系統會要求您等候一或兩分鐘的時間來完成安裝。</span><span class="sxs-lookup"><span data-stu-id="18dfe-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="18dfe-113">在安裝的最後一個階段, 會將散發版本的檔案解除壓縮並儲存在您的電腦上, 以供使用。</span><span class="sxs-lookup"><span data-stu-id="18dfe-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="18dfe-114">這可能需要一分鐘或更長的時間, 視電腦的存放裝置效能而定。</span><span class="sxs-lookup"><span data-stu-id="18dfe-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="18dfe-115">只有在清除安裝散發版本時, 才需要執行此初始安裝階段-所有未來的啟動都應該不到一秒。</span><span class="sxs-lookup"><span data-stu-id="18dfe-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="18dfe-116">設定新的 Linux 使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="18dfe-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="18dfe-117">安裝完成之後, 系統會提示您建立新的使用者帳戶 (及其密碼)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows 主控台中的 Ubuntu 解壓縮](media/UbuntuInstall.png)

<span data-ttu-id="18dfe-119">這個使用者帳戶是針對您在啟動散發版本時, 預設將登入的一般非系統管理員使用者。</span><span class="sxs-lookup"><span data-stu-id="18dfe-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="18dfe-120">您可以選擇任何您想要的使用者名稱和密碼, 而不會影響您的 Windows 使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="18dfe-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="18dfe-121">當您開啟新的散發版本實例時, 系統不會提示您輸入密碼, 但**如果您使用`sudo`** 來提高進程的許可權, 就必須輸入您的密碼, 因此請務必選擇您可以輕鬆記住的密碼!</span><span class="sxs-lookup"><span data-stu-id="18dfe-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="18dfe-122">如需詳細資訊, 請參閱[使用者支援](user-support.md)頁面。</span><span class="sxs-lookup"><span data-stu-id="18dfe-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="18dfe-123">更新 & 升級散發版本的套件</span><span class="sxs-lookup"><span data-stu-id="18dfe-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="18dfe-124">大部分的散發版本都隨附空的/最小的套件目錄。</span><span class="sxs-lookup"><span data-stu-id="18dfe-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="18dfe-125">我們強烈建議您定期更新您的套件目錄, 並使用散發版本的慣用套件管理員升級已安裝的套件。</span><span class="sxs-lookup"><span data-stu-id="18dfe-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="18dfe-126">在 Debian/Ubuntu 上, 您可以使用 apt:</span><span class="sxs-lookup"><span data-stu-id="18dfe-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="18dfe-127">Windows 不會自動更新或升級您的 Linux 散發版本:這是 Linux 使用者偏好控制自己的工作。</span><span class="sxs-lookup"><span data-stu-id="18dfe-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="18dfe-128">大功告成！</span><span class="sxs-lookup"><span data-stu-id="18dfe-128">You're done!</span></span> <span data-ttu-id="18dfe-129">在 WSL 上盡情使用您的新 Linux 散發版本!</span><span class="sxs-lookup"><span data-stu-id="18dfe-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="18dfe-130">若要深入瞭解 WSL, 請參閱其他[WSL](https://aka.ms/wsldocs)檔或[WSL learning 資源頁面](https://aka.ms/learnwsl)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![在 WSL 上享用使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="18dfe-132">疑難排解</span><span class="sxs-lookup"><span data-stu-id="18dfe-132">Troubleshooting</span></span>

<span data-ttu-id="18dfe-133">以下是相關的錯誤和建議的修正。</span><span class="sxs-lookup"><span data-stu-id="18dfe-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="18dfe-134">如需其他常見錯誤及其解決方案, 請參閱[WSL 疑難排解頁面](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="18dfe-135">**安裝失敗, 發生錯誤 0x8007007e**當您的系統不支援存放區中的 Linux 時, 就會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="18dfe-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="18dfe-136">請確認︰</span><span class="sxs-lookup"><span data-stu-id="18dfe-136">Make sure that:</span></span>
> * <span data-ttu-id="18dfe-137">您正在執行 Windows 組建16215或更新版本。</span><span class="sxs-lookup"><span data-stu-id="18dfe-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="18dfe-138">[檢查您的組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="18dfe-139">[適用于 Linux 的 Windows 子系統] 選用元件已啟用, 且電腦已重新開機。</span><span class="sxs-lookup"><span data-stu-id="18dfe-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="18dfe-140">[請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="18dfe-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
