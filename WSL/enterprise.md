---
title: 適用於 Linux for Enterprise 的 Windows 子系統
description: 有關如何在企業環境中最佳使用適用于 Linux 的 Windows 子系統的資源和指示。
keywords: BashOnWindows, bash, wsl, windows, 適用于 linux 的 windows 子系統, windowssubsystem, ubuntu, debian, suse, windows 10, 企業版, 部署, 離線, 封裝, 存放區, 散發, 安裝, 安裝
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063276"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="37390-104">適用於 Linux for Enterprise 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="37390-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="37390-105">商務用 Microsoft Store 提供各種解決方案給想要將 WSL 部署至公司的企業。</span><span class="sxs-lookup"><span data-stu-id="37390-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="37390-106">商務用 Microsoft Store 的[線上](https://docs.microsoft.com/en-us/microsoft-store/)檔, 是找出有關商店經驗的一般資訊的絕佳資源。</span><span class="sxs-lookup"><span data-stu-id="37390-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="37390-107">如果您是只想要設定開始部署 WSL 的公司, 您可以遵循下列步驟, 其會在 Microsoft Store 檔中說明:</span><span class="sxs-lookup"><span data-stu-id="37390-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="37390-108">註冊以取得商務用 Microsoft Store 並開始使用</span><span class="sxs-lookup"><span data-stu-id="37390-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="37390-109">[管理您的產品和服務 (包括誰可以存取您的私用存放區中的哪些應用程式)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。</span><span class="sxs-lookup"><span data-stu-id="37390-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="37390-110">您可以在這裡將 WSL 散發版本新增至您的存放區, 並控制可以安裝這些專案的人員</span><span class="sxs-lookup"><span data-stu-id="37390-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="37390-111">使用您選擇的散發方法, 將軟體部署至您的公司</span><span class="sxs-lookup"><span data-stu-id="37390-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="37390-112">與可存取 WSL 散發版本的使用者溝通, 他們可以[使用這些步驟](https://docs.microsoft.com/en-us/windows/wsl/install-win10)來安裝其選擇的散發版本或散發版本</span><span class="sxs-lookup"><span data-stu-id="37390-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="37390-113">如何離線散發散發版本</span><span class="sxs-lookup"><span data-stu-id="37390-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="37390-114">如果您公司中的電腦無法存取 Microsoft Store 或商務用 Microsoft Store, 您可以遵循下列步驟, 下載具有離線授權的 Linux 散發版本安裝程式。</span><span class="sxs-lookup"><span data-stu-id="37390-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="37390-115">設定 Azure Active Directory (AD) 帳戶</span><span class="sxs-lookup"><span data-stu-id="37390-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="37390-116">您需要有 Azure AD 帳戶, 而且是組織的全域管理員, 才能取得 Microsoft Store 應用程式的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="37390-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="37390-117">如果您已經有帳戶, 可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="37390-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="37390-118">您可以在這裡找到註冊帳戶的指示: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="37390-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="37390-119">登入商務用 Microsoft 並前往首頁</span><span class="sxs-lookup"><span data-stu-id="37390-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="37390-120">在此登入: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="37390-120">Sign in here: www.microsoft.com/business-store</span></span>

![商務用 MS Store 首頁](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="37390-122">移至 [管理-> 設定], 並啟用 [顯示離線應用程式]</span><span class="sxs-lookup"><span data-stu-id="37390-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![商務用 MS Store 設定頁面](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="37390-124">按一下 [購買我的群組] 以返回主要頁面</span><span class="sxs-lookup"><span data-stu-id="37390-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![商務用 MS Store 首頁](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="37390-126">搜尋您想要的散發版本並加以選取</span><span class="sxs-lookup"><span data-stu-id="37390-126">Search for your desired distro and select it</span></span>

![使用作用中搜尋的商務用 MS Store 首頁](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="37390-128">在 [授權類型] 下拉式功能表中選取「離線」授權, 然後按一下 [取得應用程式]。</span><span class="sxs-lookup"><span data-stu-id="37390-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![商務用 microsoft Store Ubuntu 產品頁面](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="37390-130">請注意: 某些散發版本可能會選擇不要擁有離線授權</span><span class="sxs-lookup"><span data-stu-id="37390-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="37390-131">按一下 [管理] 按鈕以前往應用程式的 [產品] 頁面</span><span class="sxs-lookup"><span data-stu-id="37390-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![商務用 microsoft Store Ubuntu 產品頁面](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="37390-133">選取您的架構, 並下載封裝供離線使用</span><span class="sxs-lookup"><span data-stu-id="37390-133">Select your architecture and download the package for offline use</span></span>

![商務用 microsoft Store Ubuntu 產品詳細資料頁面](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="37390-135">然後, 可以將此安裝程式散發到您想要安裝 WSL 的任何電腦。</span><span class="sxs-lookup"><span data-stu-id="37390-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>