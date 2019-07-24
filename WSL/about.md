---
title: 瞭解適用于 Linux 的 Windows 子系統
description: 深入瞭解適用于 Linux 的 Windows 子系統如何運作。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: edff78b1447aa382253417d27df52fe497c58b08
ms.sourcegitcommit: e17038c166b69f73e593ae3ac351c9d66e2ba64b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2019
ms.locfileid: "67694629"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="3a232-104">適用于 Linux 的 Windows 子系統檔</span><span class="sxs-lookup"><span data-stu-id="3a232-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="3a232-105">適用于 Linux 的 Windows 子系統可讓開發人員執行 GNU/Linux 環境 (包括大部分的命令列工具、公用程式和應用程式), 直接在 Windows 上進行修改, 而不會造成虛擬機器的額外負荷。</span><span class="sxs-lookup"><span data-stu-id="3a232-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="3a232-106">您可以：</span><span class="sxs-lookup"><span data-stu-id="3a232-106">You can:</span></span>

1. <span data-ttu-id="3a232-107">[從 Microsoft Store](https://aka.ms/wslstore)選擇您最愛的 GNU/Linux 散發套件。</span><span class="sxs-lookup"><span data-stu-id="3a232-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="3a232-108">執行一般的命令列免費軟體`grep`, 例如、 `sed`、 `awk`或其他 ELF-64 二進位檔。</span><span class="sxs-lookup"><span data-stu-id="3a232-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="3a232-109">執行 Bash shell 腳本和 GNU/Linux 命令列應用程式, 包括:</span><span class="sxs-lookup"><span data-stu-id="3a232-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="3a232-110">工具: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="3a232-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="3a232-111">語言：JAVAscript/node.js、Ruby、Python、C/C++、 C# & F#、Rust、Go 等。</span><span class="sxs-lookup"><span data-stu-id="3a232-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="3a232-112">服務: sshd、MySQL、Apache、ligHTTPd</span><span class="sxs-lookup"><span data-stu-id="3a232-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="3a232-113">使用自己的 GNU/Linux 散發套件管理員安裝其他軟體。</span><span class="sxs-lookup"><span data-stu-id="3a232-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="3a232-114">使用類似 Unix 的命令列 shell 來叫用 Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a232-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="3a232-115">在 Windows 上叫用 GNU/Linux 應用程式。</span><span class="sxs-lookup"><span data-stu-id="3a232-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="3a232-116">開始使用</span><span class="sxs-lookup"><span data-stu-id="3a232-116">Getting Started</span></span>

* [<span data-ttu-id="3a232-117">在 Windows 10 上安裝 Linux</span><span class="sxs-lookup"><span data-stu-id="3a232-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="3a232-118">流覽命令參考</span><span class="sxs-lookup"><span data-stu-id="3a232-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="3a232-119">閱讀常見問題</span><span class="sxs-lookup"><span data-stu-id="3a232-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="3a232-120">小組 Blog</span><span class="sxs-lookup"><span data-stu-id="3a232-120">Team Blogs</span></span>
*  [<span data-ttu-id="3a232-121">包含影片和 blog 集合的總覽文章</span><span class="sxs-lookup"><span data-stu-id="3a232-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="3a232-122">[命令列的 blog](https://blogs.msdn.microsoft.com/commandline/)主動</span><span class="sxs-lookup"><span data-stu-id="3a232-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="3a232-123">[適用于 Linux 的 Windows 子系統 Blog](https://blogs.msdn.microsoft.com/wsl/)歷程記錄</span><span class="sxs-lookup"><span data-stu-id="3a232-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="3a232-124">張貼 & 文章</span><span class="sxs-lookup"><span data-stu-id="3a232-124">Posts & Articles</span></span>
* [<span data-ttu-id="3a232-125">在 Windows 上的 Ubuntu 上執行 Bash</span><span class="sxs-lookup"><span data-stu-id="3a232-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="3a232-126">開發人員可以在 Windows 10 上執行 Bash 和 Usermode Ubuntu Linux 二進位檔</span><span class="sxs-lookup"><span data-stu-id="3a232-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="3a232-127">Windows 上的 ubuntu –適用于 Windows 開發人員的 Ubuntu Userspace</span><span class="sxs-lookup"><span data-stu-id="3a232-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="3a232-128">提供意見反應</span><span class="sxs-lookup"><span data-stu-id="3a232-128">Provide Feedback</span></span>
* [<span data-ttu-id="3a232-129">GitHub 問題追蹤器</span><span class="sxs-lookup"><span data-stu-id="3a232-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="3a232-130">命令列 UserVoice 入口網站</span><span class="sxs-lookup"><span data-stu-id="3a232-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
