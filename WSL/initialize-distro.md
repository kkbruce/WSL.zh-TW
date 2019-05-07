---
title: 初始化新的 WSL Linux 散發套件
description: 之後 WSL 安裝的 Linux distro，請遵循下列簡單步驟來完成初始設定
keywords: BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系統
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902045"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="bf41b-104">初始化新安裝的散發套件</span><span class="sxs-lookup"><span data-stu-id="bf41b-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="bf41b-105">一旦下載及安裝您散發版本，您必須完成初始化新的散發版本：</span><span class="sxs-lookup"><span data-stu-id="bf41b-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="bf41b-106">啟動散發版本</span><span class="sxs-lookup"><span data-stu-id="bf41b-106">Launch a distro</span></span>
<span data-ttu-id="bf41b-107">若要完成初始化的新安裝的散發版本，啟動新的執行個體。</span><span class="sxs-lookup"><span data-stu-id="bf41b-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="bf41b-108">您可以藉由按一下 Windows 市集應用程式中中的 「 啟動 」 按鈕，或啟動從 [開始] 功能表的散發版本來這樣做：</span><span class="sxs-lookup"><span data-stu-id="bf41b-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="bf41b-109">秘訣：您可能想要釘選到 [開始]，和/或工作列所做的您最常使用的散發套件 ！</span><span class="sxs-lookup"><span data-stu-id="bf41b-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![啟動散發版本，從 [開始] 功能表](media/start-menu.png)

> <span data-ttu-id="bf41b-111">在 Windows 伺服器上，您可以啟動您的散發套件的可執行檔啟動程式`<distro>.exe`從散發套件安裝資料夾。</span><span class="sxs-lookup"><span data-stu-id="bf41b-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="bf41b-112">第一次新安裝的散發套件執行的主控台視窗隨即開啟，並需要等候幾分鐘的時間才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="bf41b-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="bf41b-113">在安裝此最終階段中，發行版本的檔案取消壓縮，並儲存在您的電腦，可供使用上。</span><span class="sxs-lookup"><span data-stu-id="bf41b-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="bf41b-114">這可能需要一分鐘的時間或多個根據您的電腦的存放裝置效能。</span><span class="sxs-lookup"><span data-stu-id="bf41b-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="bf41b-115">這個初始的安裝階段只是必要的散發套件為全新安裝-所有未來的啟動花費時間少於一秒。</span><span class="sxs-lookup"><span data-stu-id="bf41b-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="bf41b-116">設定新的 Linux 使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="bf41b-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="bf41b-117">安裝完成之後，系統會提示您建立新的使用者帳戶 （和其密碼）。</span><span class="sxs-lookup"><span data-stu-id="bf41b-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![打開包裝 Windows 主控台中的 Ubuntu](media/UbuntuInstall.png)

<span data-ttu-id="bf41b-119">此使用者帳戶是一般的非系統管理員使用者，您將是已登入做為預設時啟動的散發版本。</span><span class="sxs-lookup"><span data-stu-id="bf41b-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="bf41b-120">您可以選擇任何使用者名稱和您想要的密碼-它們對您的 Windows 使用者名稱並無任何影響。</span><span class="sxs-lookup"><span data-stu-id="bf41b-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="bf41b-121">當您開啟新的散發版本執行個體時，您將不會提示您輸入密碼，但**如果您使用提升權限處理程序`sudo`，您必須輸入密碼**，因此請確定您選擇的密碼，您可輕易記住 ！</span><span class="sxs-lookup"><span data-stu-id="bf41b-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="bf41b-122">請參閱[使用者支援](user-support.md)如需詳細資訊 頁面。</span><span class="sxs-lookup"><span data-stu-id="bf41b-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="bf41b-123">更新和升級您的散發套件</span><span class="sxs-lookup"><span data-stu-id="bf41b-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="bf41b-124">大部分的散發版本隨附的最小空白/封裝目錄中。</span><span class="sxs-lookup"><span data-stu-id="bf41b-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="bf41b-125">我們強烈建議您套件的目錄，定期進行更新和升級您已安裝的套件，使用您的散發版本首選的套件管理員。</span><span class="sxs-lookup"><span data-stu-id="bf41b-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="bf41b-126">在 Debian/Ubuntu，您使用 apt 項目：</span><span class="sxs-lookup"><span data-stu-id="bf41b-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="bf41b-127">Windows 不會自動更新或升級 Linux distro(s):這是 Linux 使用者想要控制自己的工作。</span><span class="sxs-lookup"><span data-stu-id="bf41b-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="bf41b-128">大功告成！</span><span class="sxs-lookup"><span data-stu-id="bf41b-128">You're done!</span></span> <span data-ttu-id="bf41b-129">享受在 WSL 使用新的 Linux 發行版本 ！</span><span class="sxs-lookup"><span data-stu-id="bf41b-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="bf41b-130">若要深入了解 WSL，檢閱另[WSL docs](https://aka.ms/wsldocs)，或有[WSL 學習資源頁面](https://aka.ms/learnwsl)。</span><span class="sxs-lookup"><span data-stu-id="bf41b-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![享受 WSL 上使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="bf41b-132">疑難排解</span><span class="sxs-lookup"><span data-stu-id="bf41b-132">Troubleshooting</span></span>

<span data-ttu-id="bf41b-133">以下是相關的錯誤和建議的修正。</span><span class="sxs-lookup"><span data-stu-id="bf41b-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="bf41b-134">請參閱[WSL 疑難排解頁面](troubleshooting.md)其他常見的錯誤和他們的解決方案。</span><span class="sxs-lookup"><span data-stu-id="bf41b-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="bf41b-135">**安裝失敗，錯誤 0x8007007e**系統不支援 Linux，從存放區時，會發生此錯誤。</span><span class="sxs-lookup"><span data-stu-id="bf41b-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="bf41b-136">請確認︰</span><span class="sxs-lookup"><span data-stu-id="bf41b-136">Make sure that:</span></span>
> * <span data-ttu-id="bf41b-137">您正在執行 Windows 組建，16215 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bf41b-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="bf41b-138">[請檢查您的組建](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="bf41b-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="bf41b-139">已啟用 Linux 選擇性元件的 Windows 子系統，並重新啟動電腦。</span><span class="sxs-lookup"><span data-stu-id="bf41b-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="bf41b-140">[請確定已啟用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="bf41b-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
