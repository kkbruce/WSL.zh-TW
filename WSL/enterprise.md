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
# <a name="windows-subsystem-for-linux-for-enterprise"></a>適用於 Linux for Enterprise 的 Windows 子系統

商務用 Microsoft Store 提供各種解決方案給想要將 WSL 部署至公司的企業。 商務用 Microsoft Store 的[線上](https://docs.microsoft.com/en-us/microsoft-store/)檔, 是找出有關商店經驗的一般資訊的絕佳資源。

如果您是只想要設定開始部署 WSL 的公司, 您可以遵循下列步驟, 其會在 Microsoft Store 檔中說明:

* [註冊以取得商務用 Microsoft Store 並開始使用](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [管理您的產品和服務 (包括誰可以存取您的私用存放區中的哪些應用程式)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。 您可以在這裡將 WSL 散發版本新增至您的存放區, 並控制可以安裝這些專案的人員
* [使用您選擇的散發方法, 將軟體部署至您的公司](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 與可存取 WSL 散發版本的使用者溝通, 他們可以[使用這些步驟](https://docs.microsoft.com/en-us/windows/wsl/install-win10)來安裝其選擇的散發版本或散發版本 

## <a name="how-to-distribute-a-distro-offline"></a>如何離線散發散發版本

如果您公司中的電腦無法存取 Microsoft Store 或商務用 Microsoft Store, 您可以遵循下列步驟, 下載具有離線授權的 Linux 散發版本安裝程式。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>設定 Azure Active Directory (AD) 帳戶 

您需要有 Azure AD 帳戶, 而且是組織的全域管理員, 才能取得 Microsoft Store 應用程式的安裝程式。 如果您已經有帳戶, 可以略過此步驟。

您可以在這裡找到註冊帳戶的指示: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>登入商務用 Microsoft 並前往首頁
在此登入: www.microsoft.com/business-store

![商務用 MS Store 首頁](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>移至 [管理-> 設定], 並啟用 [顯示離線應用程式]

![商務用 MS Store 設定頁面](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>按一下 [購買我的群組] 以返回主要頁面

![商務用 MS Store 首頁](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>搜尋您想要的散發版本並加以選取

![使用作用中搜尋的商務用 MS Store 首頁](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>在 [授權類型] 下拉式功能表中選取「離線」授權, 然後按一下 [取得應用程式]。

![商務用 microsoft Store Ubuntu 產品頁面](media/offlineinstallscreens/4-screen.png)

請注意: 某些散發版本可能會選擇不要擁有離線授權

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>按一下 [管理] 按鈕以前往應用程式的 [產品] 頁面

![商務用 microsoft Store Ubuntu 產品頁面](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>選取您的架構, 並下載封裝供離線使用

![商務用 microsoft Store Ubuntu 產品詳細資料頁面](media/offlineinstallscreens/6-screen.png)

然後, 可以將此安裝程式散發到您想要安裝 WSL 的任何電腦。