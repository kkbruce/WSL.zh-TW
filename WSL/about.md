---
title: 瞭解適用於 Linux 的 Windows 子系統
description: 深入了解適用於 Linux 的 Windows 子系統的運作方式。
keywords: BashOnWindows，bash，wsl、 windows、 windowssubsystem、 gnu、 linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040811"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="d37db-104">Linux 文件的 Windows 子系統</span><span class="sxs-lookup"><span data-stu-id="d37db-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="d37db-105">適用於 Linux 的 Windows 子系統會讓執行-包括大部分的命令列工具、 公用程式和應用程式-GNU/Linux 環境的開發人員直接在 Windows 中，未經修改，無需額外的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="d37db-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="d37db-106">您可以：</span><span class="sxs-lookup"><span data-stu-id="d37db-106">You can:</span></span>

1. <span data-ttu-id="d37db-107">選擇您最愛的 GNU/Linux 散發[從 Windows 市集](https://aka.ms/wslstore)。</span><span class="sxs-lookup"><span data-stu-id="d37db-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="d37db-108">執行一般命令列的免費軟體，例如`grep`， `sed`， `awk`，或其他 ELF-64 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="d37db-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="d37db-109">執行 Bash 殼層指令碼和 GNU/Linux 命令列應用程式，包括：</span><span class="sxs-lookup"><span data-stu-id="d37db-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="d37db-110">工具： vim、 emacs、 tmux</span><span class="sxs-lookup"><span data-stu-id="d37db-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="d37db-111">語言：Javascript/node.js、 Ruby、 Python、 C /C++， C# & F#、 Rust、 Go 等等。</span><span class="sxs-lookup"><span data-stu-id="d37db-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="d37db-112">服務： sshd，MySQL，Apache，lighttpd</span><span class="sxs-lookup"><span data-stu-id="d37db-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="d37db-113">安裝其他軟體，使用自己的 GNU/Linux 散發套件管理員。</span><span class="sxs-lookup"><span data-stu-id="d37db-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="d37db-114">叫用使用 Unix 型的命令列殼層的 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d37db-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="d37db-115">叫用 Windows 上的 GNU/Linux 應用程式。</span><span class="sxs-lookup"><span data-stu-id="d37db-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d37db-116">開始使用</span><span class="sxs-lookup"><span data-stu-id="d37db-116">Getting Started</span></span>

* [<span data-ttu-id="d37db-117">Windows 10 上安裝 Linux</span><span class="sxs-lookup"><span data-stu-id="d37db-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="d37db-118">請瀏覽命令參考</span><span class="sxs-lookup"><span data-stu-id="d37db-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="d37db-119">閱讀常見問題集</span><span class="sxs-lookup"><span data-stu-id="d37db-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="d37db-120">小組部落格</span><span class="sxs-lookup"><span data-stu-id="d37db-120">Team Blogs</span></span>
*  [<span data-ttu-id="d37db-121">概觀文章與影片和部落格的集合</span><span class="sxs-lookup"><span data-stu-id="d37db-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="d37db-122">[命令列的部落格](https://blogs.msdn.microsoft.com/commandline/)(Active)</span><span class="sxs-lookup"><span data-stu-id="d37db-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="d37db-123">[Linux 的部落格的 Windows 子系統](https://blogs.msdn.microsoft.com/wsl/)（歷史）</span><span class="sxs-lookup"><span data-stu-id="d37db-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="d37db-124">文章與文章</span><span class="sxs-lookup"><span data-stu-id="d37db-124">Posts & Articles</span></span>
* [<span data-ttu-id="d37db-125">執行的 Bash on Ubuntu on Windows</span><span class="sxs-lookup"><span data-stu-id="d37db-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="d37db-126">開發人員可以在 Windows 10 上執行 Bash 和 Usermode Ubuntu Linux 二進位檔</span><span class="sxs-lookup"><span data-stu-id="d37db-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="d37db-127">Ubuntu on Windows-適用於 Windows 開發人員 Ubuntu Userspace</span><span class="sxs-lookup"><span data-stu-id="d37db-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="d37db-128">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="d37db-128">Provide Feedback</span></span>
* [<span data-ttu-id="d37db-129">GitHub 問題追蹤程式</span><span class="sxs-lookup"><span data-stu-id="d37db-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="d37db-130">命令列的 UserVoice 入口網站</span><span class="sxs-lookup"><span data-stu-id="d37db-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
