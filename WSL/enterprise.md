---
title: 適用於 Linux for Enterprise 的 Windows 子系統
description: 資源，以及指示如何充分使用適用於 Linux 的 Windows 子系統在企業環境中。
keywords: 安裝 BashOnWindows、 bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10、 enterprise、 部署、 離線、 封裝、 存放區、 發佈、 安裝的 windows 子系統
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063276"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>適用於 Linux for Enterprise 的 Windows 子系統

Microsoft Store for Business 到想要為其公司部署 WSL 的企業提供各式各樣的解決方案。 [線上文件](https://docs.microsoft.com/en-us/microsoft-store/)為 Microsoft Store for Business 的 若要了解的市集體驗的一般資訊的絕佳資源。

如果您是一家公司，只想要設定註冊好開始部署 WSL 您可以遵循下列步驟，會說明在 Microsoft Store 文件內：

* [註冊 Microsoft Store for Business，並開始使用](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [管理您的產品和服務 （包括誰可以存取哪些應用程式，在您的私人市集）](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。 此處新增 WSL 散發版本，以及在您的存放區和控制可以安裝它們
* [將軟體部署到您的公司使用您選擇發佈方法](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 具有存取權，他們可以 WSL 散發版本的使用者進行通訊[使用下列步驟](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安裝發行版本或其所選的散發套件 

## <a name="how-to-distribute-a-distro-offline"></a>如何發佈的 Distro 離線

如果您的公司中的電腦沒有 Microsoft Store 或 Microsoft Store for Business 的存取權，您可以下載依照這些步驟已離線授權的 Linux distro 的安裝程式。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>設定 Azure Active Directory (AD) 帳戶 

您需要有 Azure AD 帳戶，而且是為您的組織取得 Microsoft Store 應用程式的安裝程式的全域管理員。 如果您已經有帳戶，您可以略過此步驟。

若要註冊帳戶的指示可在這裡找到： https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>企業登入存放區，並移至首頁
在此登入： www.microsoft.com/business-store

![MS Store 公司首頁](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>移至 管理-> 設定並啟用 顯示離線應用程式

![MS Store for business 設定 頁面](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>返回主要頁面，依序按一下 '購買我的群組'

![MS Store 公司首頁](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>搜尋您想要的發行版本，並加以選取

![使用作用中的搜尋服務的公司首頁的 MS Store](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>授權類型下拉式選單中選取 'Offline' 授權，然後按一下 取得應用程式'

![MS Store for business Ubuntu 產品頁面](media/offlineinstallscreens/4-screen.png)

請注意： 某些散發套件可能會選擇不讓離線授權

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>按一下 [管理] 按鈕以移至應用程式的產品頁面

![MS Store for business Ubuntu 產品頁面](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>選取您的架構，並下載離線使用的套件

![MS Store for business Ubuntu 產品詳細資料頁面](media/offlineinstallscreens/6-screen.png)

此安裝程式便可分配至您想要安裝 WSL 的任何電腦。