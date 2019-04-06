---
title: 適用於 Enterprise Linux 的 Windows 子系統
description: 資源，以及指示如何充分使用適用於 Linux 的 Windows 子系統在企業環境中。
keywords: 安裝 BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10、 enterprise、 部署、 離線、 封裝、 存放區、 發佈、 安裝的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063276"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="3d914-104">適用於 Enterprise Linux 的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="3d914-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="3d914-105">Microsoft Store for Business 到想要為其公司部署 WSL 的企業提供各式各樣的解決方案。</span><span class="sxs-lookup"><span data-stu-id="3d914-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="3d914-106">[線上文件](https://docs.microsoft.com/en-us/microsoft-store/)為 Microsoft Store for Business 的 若要了解的市集體驗的一般資訊的絕佳資源。</span><span class="sxs-lookup"><span data-stu-id="3d914-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="3d914-107">如果您是一家公司，只想要設定註冊好開始部署 WSL 您可以遵循下列步驟，會說明在 Microsoft Store 文件內：</span><span class="sxs-lookup"><span data-stu-id="3d914-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="3d914-108">註冊 Microsoft Store for Business，並開始使用</span><span class="sxs-lookup"><span data-stu-id="3d914-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="3d914-109">[管理您的產品和服務 （包括誰可以存取哪些應用程式，在您的私人市集）](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。</span><span class="sxs-lookup"><span data-stu-id="3d914-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="3d914-110">此處新增 WSL 散發版本，以及在您的存放區和控制可以安裝它們</span><span class="sxs-lookup"><span data-stu-id="3d914-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="3d914-111">將軟體部署到您的公司使用您選擇發佈方法</span><span class="sxs-lookup"><span data-stu-id="3d914-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="3d914-112">具有存取權，他們可以 WSL 散發版本的使用者進行通訊[使用下列步驟](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安裝發行版本或其所選的散發套件</span><span class="sxs-lookup"><span data-stu-id="3d914-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="3d914-113">如何發佈的 Distro 離線</span><span class="sxs-lookup"><span data-stu-id="3d914-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="3d914-114">如果您的公司中的電腦沒有 Microsoft Store 或 Microsoft Store for Business 的存取權，您可以下載依照這些步驟已離線授權的 Linux distro 的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="3d914-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="3d914-115">設定 Azure Active Directory (AD) 帳戶</span><span class="sxs-lookup"><span data-stu-id="3d914-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="3d914-116">您需要有 Azure AD 帳戶，而且是為您的組織取得 Microsoft Store 應用程式的安裝程式的全域管理員。</span><span class="sxs-lookup"><span data-stu-id="3d914-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="3d914-117">如果您已經有帳戶，您可以略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="3d914-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="3d914-118">若要註冊帳戶的指示可在這裡找到： https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="3d914-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="3d914-119">企業登入存放區，並移至首頁</span><span class="sxs-lookup"><span data-stu-id="3d914-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="3d914-120">在此登入： www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="3d914-120">Sign in here: www.microsoft.com/business-store</span></span>

![MS Store 公司首頁](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="3d914-122">移至 管理-> 設定並啟用 顯示離線應用程式</span><span class="sxs-lookup"><span data-stu-id="3d914-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![MS Store for business 設定 頁面](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="3d914-124">返回主要頁面，依序按一下 '購買我的群組'</span><span class="sxs-lookup"><span data-stu-id="3d914-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![MS Store 公司首頁](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="3d914-126">搜尋您想要的發行版本，並加以選取</span><span class="sxs-lookup"><span data-stu-id="3d914-126">Search for your desired distro and select it</span></span>

![使用作用中的搜尋服務的公司首頁的 MS Store](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="3d914-128">授權類型下拉式選單中選取 'Offline' 授權，然後按一下 取得應用程式'</span><span class="sxs-lookup"><span data-stu-id="3d914-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS Store for business Ubuntu 產品頁面](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="3d914-130">請注意： 某些散發套件可能會選擇不讓離線授權</span><span class="sxs-lookup"><span data-stu-id="3d914-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="3d914-131">按一下 [管理] 按鈕以移至應用程式的產品頁面</span><span class="sxs-lookup"><span data-stu-id="3d914-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS Store for business Ubuntu 產品頁面](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="3d914-133">選取您的架構，並下載離線使用的套件</span><span class="sxs-lookup"><span data-stu-id="3d914-133">Select your architecture and download the package for offline use</span></span>

![MS Store for business Ubuntu 產品詳細資料頁面](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="3d914-135">此安裝程式便可分配至您想要安裝 WSL 的任何電腦。</span><span class="sxs-lookup"><span data-stu-id="3d914-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>