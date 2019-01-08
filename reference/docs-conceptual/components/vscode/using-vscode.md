---
title: 使用 Visual Studio Code 进行 PowerShell 开发
description: 使用 Visual Studio Code 进行 PowerShell 开发
ms.date: 08/06/2018
ms.openlocfilehash: 3101fa57896996a696385801303333e4a6406d20
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2018
ms.locfileid: "53400383"
---
# <a name="using-visual-studio-code-for-powershell-development"></a><span data-ttu-id="82c95-103">使用 Visual Studio Code 进行 PowerShell 开发</span><span class="sxs-lookup"><span data-stu-id="82c95-103">Using Visual Studio Code for PowerShell Development</span></span>

<span data-ttu-id="82c95-104">除 [PowerShell ISE][ise] 外，PowerShell 还高度支持 Visual Studio Code。</span><span class="sxs-lookup"><span data-stu-id="82c95-104">In addition to the [PowerShell ISE][ise], PowerShell is also well-supported in Visual Studio Code.</span></span>
<span data-ttu-id="82c95-105">此外，PowerShell Core 不支持 ISE，但是 Visual Studio Code 在所有平台上（Windows、macOS 和 Linux）均支持 PowerShell Core</span><span class="sxs-lookup"><span data-stu-id="82c95-105">Furthermore, the ISE is not supported with PowerShell Core, while Visual Studio Code is supported for PowerShell Core on all platforms (Windows, macOS, and Linux)</span></span>

<span data-ttu-id="82c95-106">通过使用 Windows 10 或安装适用于低版本 Windows OS（例如 Windows 8.1 等）的 [Windows Management Framework 5.0 RTM](https://www.microsoft.com/en-us/download/details.aspx?id=50395)，可在 Windows 上结合使用 Visual Studio Code 和 PowerShell 版本 5.</span><span class="sxs-lookup"><span data-stu-id="82c95-106">You can use Visual Studio Code on Windows with PowerShell version 5 by using Windows 10 or by installing [Windows Management Framework 5.0 RTM](https://www.microsoft.com/en-us/download/details.aspx?id=50395) for down-level Windows OSs (e.g. Windows 8.1, etc.).</span></span>

<span data-ttu-id="82c95-107">开始前，请确保系统上安装有 PowerShell。</span><span class="sxs-lookup"><span data-stu-id="82c95-107">Before starting it, please make sure PowerShell exists on your system.</span></span>
<span data-ttu-id="82c95-108">有关 Windows、macOS 和 Linux 上的新式工作负荷，请参阅：</span><span class="sxs-lookup"><span data-stu-id="82c95-108">For modern workloads on Windows, macOS, and Linux, see:</span></span>

- <span data-ttu-id="82c95-109">[在 Linux 上安装 PowerShell Core][install-pscore-linux]</span><span class="sxs-lookup"><span data-stu-id="82c95-109">[Installing PowerShell Core on Linux][install-pscore-linux]</span></span>
- <span data-ttu-id="82c95-110">[在 macOS 上安装 PowerShell Core][install-pscore-macos]</span><span class="sxs-lookup"><span data-stu-id="82c95-110">[Installing PowerShell Core on macOS][install-pscore-macos]</span></span>
- <span data-ttu-id="82c95-111">[在 Windows 上安装 PowerShell Core][install-pscore-windows]</span><span class="sxs-lookup"><span data-stu-id="82c95-111">[Installing PowerShell Core on Windows][install-pscore-windows]</span></span>

<span data-ttu-id="82c95-112">有关传统 Windows PowerShell 工作负荷，请参阅[安装 Windows PowerShell][install-winps]。</span><span class="sxs-lookup"><span data-stu-id="82c95-112">For traditional Windows PowerShell workloads, see [Installing Windows PowerShell][install-winps].</span></span>

## <a name="editing-with-visual-studio-code"></a><span data-ttu-id="82c95-113">使用 Visual Studio Code 进行编辑</span><span class="sxs-lookup"><span data-stu-id="82c95-113">Editing with Visual Studio Code</span></span>

### <a name="1-installing-visual-studio-codehttpscodevisualstudiocomdocssetupsetup-overview"></a>[<span data-ttu-id="82c95-114">1.安装 Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="82c95-114">1. Installing Visual Studio Code</span></span>](https://code.visualstudio.com/Docs/setup/setup-overview)

- <span data-ttu-id="82c95-115">**Linux**：请按照[在 Linux 上运行 VS Code](https://code.visualstudio.com/docs/setup/linux) 页面上的安装说明进行操作</span><span class="sxs-lookup"><span data-stu-id="82c95-115">**Linux**: follow the installation instructions on the [Running VS Code on Linux](https://code.visualstudio.com/docs/setup/linux) page</span></span>

- <span data-ttu-id="82c95-116">**macOS**：请按照[在 macOS 上运行 VS Code](https://code.visualstudio.com/docs/setup/mac) 页面上的安装说明进行操作</span><span class="sxs-lookup"><span data-stu-id="82c95-116">**macOS**: follow the installation instructions on the [Running VS Code on macOS](https://code.visualstudio.com/docs/setup/mac) page</span></span>

  > [!IMPORTANT]
  > <span data-ttu-id="82c95-117">在 macOS 上，必须安装 OpenSSL 后 PowerShell 扩展方可正常运行。</span><span class="sxs-lookup"><span data-stu-id="82c95-117">On macOS, you must install OpenSSL for the PowerShell extension to work correctly.</span></span>
  > <span data-ttu-id="82c95-118">实现此要求的最简单方法是安装 [Homebrew](https://brew.sh/)，然后运行 `brew install openssl`。</span><span class="sxs-lookup"><span data-stu-id="82c95-118">The easiest way to accomplish this is to install [Homebrew](https://brew.sh/) and then run `brew install openssl`.</span></span>
  > <span data-ttu-id="82c95-119">VS Code 现可成功加载 PowerShell 扩展。</span><span class="sxs-lookup"><span data-stu-id="82c95-119">VS Code can now load the PowerShell extension successfully.</span></span>

- <span data-ttu-id="82c95-120">**Windows**：按照[在 Windows 上运行 VS Code](https://code.visualstudio.com/docs/setup/windows) 页面上的安装说明进行操作</span><span class="sxs-lookup"><span data-stu-id="82c95-120">**Windows**: follow the installation instructions on the [Running VS Code on Windows](https://code.visualstudio.com/docs/setup/windows) page</span></span>

### <a name="2-installing-powershell-extension"></a><span data-ttu-id="82c95-121">2.安装 PowerShell 扩展</span><span class="sxs-lookup"><span data-stu-id="82c95-121">2. Installing PowerShell Extension</span></span>

- <span data-ttu-id="82c95-122">按照如下方式启动 Visual Studio Code 应用：</span><span class="sxs-lookup"><span data-stu-id="82c95-122">Launch the Visual Studio Code app by:</span></span>
  - <span data-ttu-id="82c95-123">**Windows**：在 PowerShell 会话中键入 `code`</span><span class="sxs-lookup"><span data-stu-id="82c95-123">**Windows**: typing `code` in your PowerShell session</span></span>
  - <span data-ttu-id="82c95-124">**Linux**：在终端中键入 `code`</span><span class="sxs-lookup"><span data-stu-id="82c95-124">**Linux**: typing `code` in your terminal</span></span>
  - <span data-ttu-id="82c95-125">**macOS**：在终端中键入 `code`</span><span class="sxs-lookup"><span data-stu-id="82c95-125">**macOS**: typing `code` in your terminal</span></span>

- <span data-ttu-id="82c95-126">通过按 Ctrl+P（Mac 上为 Cmd+P）启动“Quick Open”。</span><span class="sxs-lookup"><span data-stu-id="82c95-126">Launch **Quick Open** by pressing **Ctrl+P** (**Cmd+P** on Mac).</span></span>
- <span data-ttu-id="82c95-127">在“Quick Open”中，键入 `ext install powershell` 并按 Enter。</span><span class="sxs-lookup"><span data-stu-id="82c95-127">In Quick Open, type `ext install powershell` and hit **Enter**.</span></span>
- <span data-ttu-id="82c95-128">“扩展”视图随即在侧边栏上打开。</span><span class="sxs-lookup"><span data-stu-id="82c95-128">The **Extensions** view opens on the Side Bar.</span></span> <span data-ttu-id="82c95-129">从 Microsoft 中选择 PowerShell 扩展。</span><span class="sxs-lookup"><span data-stu-id="82c95-129">Select the PowerShell extension from Microsoft.</span></span>
  <span data-ttu-id="82c95-130">应看到如下内容：</span><span class="sxs-lookup"><span data-stu-id="82c95-130">You should see something like below:</span></span>

  ![VSCode](../../images/vscode.png)

- <span data-ttu-id="82c95-132">在 Microsoft 下单击 PowerShell 扩展上的“安装”按钮。</span><span class="sxs-lookup"><span data-stu-id="82c95-132">Click the **Install** button on the PowerShell extension from Microsoft.</span></span>
- <span data-ttu-id="82c95-133">安装后，“安装”按钮将变为“重载”。</span><span class="sxs-lookup"><span data-stu-id="82c95-133">After the install, you see the **Install** button turns to **Reload**.</span></span>
  <span data-ttu-id="82c95-134">单击“重载”。</span><span class="sxs-lookup"><span data-stu-id="82c95-134">Click on **Reload**.</span></span>
- <span data-ttu-id="82c95-135">重载 Visual Studio Code 后即可开始编辑。</span><span class="sxs-lookup"><span data-stu-id="82c95-135">After Visual Studio Code has reload, you are ready for editing.</span></span>

<span data-ttu-id="82c95-136">例如，若要创建新文件，请单击“文件”->“新建”。</span><span class="sxs-lookup"><span data-stu-id="82c95-136">For example, to create a new file, click **File->New**.</span></span>
<span data-ttu-id="82c95-137">若要保存，请单击“文件”->“保存”，然后提供一个文件名，例如 `HelloWorld.ps1`。</span><span class="sxs-lookup"><span data-stu-id="82c95-137">To save it, click **File->Save** and then provide a file name, let's say `HelloWorld.ps1`.</span></span>
<span data-ttu-id="82c95-138">若要关闭文件，则单击文件名旁的“x”。</span><span class="sxs-lookup"><span data-stu-id="82c95-138">To close the file, click on "x" next to the file name.</span></span>
<span data-ttu-id="82c95-139">若要退出 Visual Studio Code，请单击“文件”->“退出”。</span><span class="sxs-lookup"><span data-stu-id="82c95-139">To exit Visual Studio Code, **File->Exit**.</span></span>

#### <a name="using-a-specific-installed-version-of-powershell"></a><span data-ttu-id="82c95-140">使用 PowerShell 特定安装版</span><span class="sxs-lookup"><span data-stu-id="82c95-140">Using a specific installed version of PowerShell</span></span>

<span data-ttu-id="82c95-141">如果要通过 Visual Studio Code 使用 PowerShell 的特定安装版，则需要将新的变量添加到用户设置文件。</span><span class="sxs-lookup"><span data-stu-id="82c95-141">If you wish to use a specific installation of PowerShell with Visual Studio Code, you need to add a new variable to your user settings file.</span></span>

1. <span data-ttu-id="82c95-142">单击“文件”->“首选项”->“设置”</span><span class="sxs-lookup"><span data-stu-id="82c95-142">Click **File -> Preferences -> Settings**</span></span>
1. <span data-ttu-id="82c95-143">此时会出现两个编辑器窗格。</span><span class="sxs-lookup"><span data-stu-id="82c95-143">Two editor panes appear.</span></span>
   <span data-ttu-id="82c95-144">在最右侧窗格 (`settings.json`) 中，在两个花括号（`{` 和 `}`）之间的某处插入下面的 OS 对应设置，并将 \<版本\> 替换为已安装的 PowerShell 版本：</span><span class="sxs-lookup"><span data-stu-id="82c95-144">In the right-most pane (`settings.json`), insert the setting below appropriate for your OS somewhere between the two curly brackets (`{` and `}`) and replace **\<version\>** with the installed PowerShell version:</span></span>

   ```json
    // On Windows:
    "powershell.powerShellExePath": "c:/Program Files/PowerShell/<version>/pwsh.exe"

    // On Linux:
    "powershell.powerShellExePath": "/opt/microsoft/powershell/<version>/pwsh"

    // On macOS:
    "powershell.powerShellExePath": "/usr/local/microsoft/powershell/<version>/pwsh"
   ```

1. <span data-ttu-id="82c95-145">将设置替换为所需 PowerShell 可执行文件的路径</span><span class="sxs-lookup"><span data-stu-id="82c95-145">Replace the setting with the path to the desired PowerShell executable</span></span>
1. <span data-ttu-id="82c95-146">保存设置文件并重启 Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="82c95-146">Save the settings file and restart Visual Studio Code</span></span>

#### <a name="configuration-settings-for-visual-studio-code"></a><span data-ttu-id="82c95-147">Visual Studio Code 的配置设置</span><span class="sxs-lookup"><span data-stu-id="82c95-147">Configuration settings for Visual Studio Code</span></span>

<span data-ttu-id="82c95-148">按照上一段落中的步骤可在 `settings.json` 中添加配置设置。</span><span class="sxs-lookup"><span data-stu-id="82c95-148">By using the steps in the previous paragraph you can add configuration settings in `settings.json`.</span></span>

<span data-ttu-id="82c95-149">我们建议对 Visual Studio Code 添加以下配置设置：</span><span class="sxs-lookup"><span data-stu-id="82c95-149">We recommend the following configuration settings for Visual Studio Code:</span></span>

```json
{
    "csharp.suppressDotnetRestoreNotification": true,
    "editor.renderWhitespace": "all",
    "editor.renderControlCharacters": true,
    "omnisharp.projectLoadTimeout": 120,
    "files.trimTrailingWhitespace": true
}
```

## <a name="debugging-with-visual-studio-code"></a><span data-ttu-id="82c95-150">使用 Visual Studio Code 进行调试</span><span class="sxs-lookup"><span data-stu-id="82c95-150">Debugging with Visual Studio Code</span></span>

### <a name="no-workspace-debugging"></a><span data-ttu-id="82c95-151">无工作区调试</span><span class="sxs-lookup"><span data-stu-id="82c95-151">No-workspace debugging</span></span>

<span data-ttu-id="82c95-152">从 Visual Studio Code 版本 1.9 开始，无需打开包含 PowerShell 脚本的文件夹即可调试 PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="82c95-152">As of Visual Studio Code version 1.9 you can debug PowerShell scripts without having to open the folder containing the PowerShell script.</span></span>
<span data-ttu-id="82c95-153">只需单击“文件”->“打开文件...”打开 PowerShell 脚本文件，在行上设一个断点（按 F9），然后按 F5 即可开始调试。</span><span class="sxs-lookup"><span data-stu-id="82c95-153">Simply open the PowerShell script file with **File->Open File...**, set a breakpoint on a line (press F9) and then press F5 to start debugging.</span></span>
<span data-ttu-id="82c95-154">此时应出现“调试”操作窗格，通过该窗格可以中断调试器、执行、继续和停止调试。</span><span class="sxs-lookup"><span data-stu-id="82c95-154">You should see the Debug actions pane appear which allows you to break into the debugger, step, resume and stop debugging.</span></span>

### <a name="workspace-debugging"></a><span data-ttu-id="82c95-155">工作区调试</span><span class="sxs-lookup"><span data-stu-id="82c95-155">Workspace debugging</span></span>

<span data-ttu-id="82c95-156">工作区调试是指文件夹上下文中的调试，该文件夹是使用“文件”菜单的“打开文件夹...”在 Visual Studio Code 中打开的。</span><span class="sxs-lookup"><span data-stu-id="82c95-156">Workspace debugging refers to debugging in the context of a folder that you have opened in Visual Studio Code using **Open Folder...** from the **File** menu.</span></span>
<span data-ttu-id="82c95-157">打开的文件夹通常是 PowerShell 项目文件夹和/或 Git 存储库的根文件夹。</span><span class="sxs-lookup"><span data-stu-id="82c95-157">The folder you open is typically your PowerShell project folder and/or the root of your Git repository.</span></span>

<span data-ttu-id="82c95-158">即使在此模式下，按 F5 也可开始调试当前所选的 PowerShell 脚本。</span><span class="sxs-lookup"><span data-stu-id="82c95-158">Even in this mode, you can start debugging the currently selected PowerShell script by simply pressing F5.</span></span>
<span data-ttu-id="82c95-159">但是，通过工作区调试可以定义多个调试配置，而不是只调试当前打开的文件。</span><span class="sxs-lookup"><span data-stu-id="82c95-159">However, workspace debugging allows you to define multiple debug configurations other than just debugging the currently open file.</span></span>
<span data-ttu-id="82c95-160">例如，可通过添加配置执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="82c95-160">For instance, you can add a configurations to:</span></span>

- <span data-ttu-id="82c95-161">在调试器中启动 Pester 测试</span><span class="sxs-lookup"><span data-stu-id="82c95-161">Launch Pester tests in the debugger</span></span>
- <span data-ttu-id="82c95-162">使用调试器中的参数启动特定文件</span><span class="sxs-lookup"><span data-stu-id="82c95-162">Launch a specific file with arguments in the debugger</span></span>
- <span data-ttu-id="82c95-163">在调试器中启动交互会话</span><span class="sxs-lookup"><span data-stu-id="82c95-163">Launch an interactive session in the debugger</span></span>
- <span data-ttu-id="82c95-164">将调试器附加到 PowerShell 主机进程</span><span class="sxs-lookup"><span data-stu-id="82c95-164">Attach the debugger to a PowerShell host process</span></span>

<span data-ttu-id="82c95-165">按照以下步骤创建调试配置文件：</span><span class="sxs-lookup"><span data-stu-id="82c95-165">Follow these steps to create your debug configuration file:</span></span>

  1. <span data-ttu-id="82c95-166">按 Ctrl+Shift+D（Mac 上为 Cmd+Shift+D）打开“调试”视图。</span><span class="sxs-lookup"><span data-stu-id="82c95-166">Open the **Debug** view by pressing **Ctrl+Shift+D** (**Cmd+Shift+D** on Mac).</span></span>
  2. <span data-ttu-id="82c95-167">按工具栏中的“配置”齿轮图标。</span><span class="sxs-lookup"><span data-stu-id="82c95-167">Press the **Configure** gear icon in the toolbar.</span></span>
  3. <span data-ttu-id="82c95-168">Visual Studio Code 将提示“选择环境”。</span><span class="sxs-lookup"><span data-stu-id="82c95-168">Visual Studio Code prompts you to **Select Environment**.</span></span> <span data-ttu-id="82c95-169">选择“PowerShell”。</span><span class="sxs-lookup"><span data-stu-id="82c95-169">Choose **PowerShell**.</span></span>

  <span data-ttu-id="82c95-170">执行此操作时，Visual Studio Code 会在工作区文件夹的根中创建一个目录和一个“.vscode\launch.json”文件。</span><span class="sxs-lookup"><span data-stu-id="82c95-170">When you do this, Visual Studio Code creates a directory and a file ".vscode\launch.json" in the root of your workspace folder.</span></span>
  <span data-ttu-id="82c95-171">这是调试配置的存储位置。</span><span class="sxs-lookup"><span data-stu-id="82c95-171">This is where your debug configuration is stored.</span></span> <span data-ttu-id="82c95-172">如果文件位于 Git 存储库中，则通常需要提交 launch.json 文件。</span><span class="sxs-lookup"><span data-stu-id="82c95-172">If your files are in a Git repository, you typically want to commit the launch.json file.</span></span>
  <span data-ttu-id="82c95-173">launch.json 文件的内容为：</span><span class="sxs-lookup"><span data-stu-id="82c95-173">The contents of the launch.json file are:</span></span>

  ```json
  {
    "version": "0.2.0",
    "configurations": [
        {
            "type": "PowerShell",
            "request": "launch",
            "name": "PowerShell Launch (current file)",
            "script": "${file}",
            "args": [],
            "cwd": "${file}"
        },
        {
            "type": "PowerShell",
            "request": "attach",
            "name": "PowerShell Attach to Host Process",
            "processId": "${command.PickPSHostProcess}",
            "runspaceId": 1
        },
        {
            "type": "PowerShell",
            "request": "launch",
            "name": "PowerShell Interactive Session",
            "cwd": "${workspaceRoot}"
        }
    ]
  }
  ```

  <span data-ttu-id="82c95-174">这表示常见调试方案。</span><span class="sxs-lookup"><span data-stu-id="82c95-174">This represents the common debug scenarios.</span></span>
  <span data-ttu-id="82c95-175">但是，在编辑器中打开此文件时，会显示“添加配置...”按钮。</span><span class="sxs-lookup"><span data-stu-id="82c95-175">However, when you open this file in the editor, you see an **Add Configuration...** button.</span></span>
  <span data-ttu-id="82c95-176">按此按钮可添加更多 PowerShell 调试配置。</span><span class="sxs-lookup"><span data-stu-id="82c95-176">You can press this button to add more PowerShell debug configurations.</span></span> <span data-ttu-id="82c95-177">若要添加的一个便捷配置是**PowerShell:启动脚本**。</span><span class="sxs-lookup"><span data-stu-id="82c95-177">One handy configuration to add is **PowerShell: Launch Script**.</span></span>
  <span data-ttu-id="82c95-178">通过此配置，可以使用可选参数指定特定文件，无论编辑器中哪个文件处于活动状态，无论何时按 F5 时，此文件都会启动。</span><span class="sxs-lookup"><span data-stu-id="82c95-178">With this configuration, you can specify a specific file with optional arguments that should be launched whenever you press F5 no matter which file is currently active in the editor.</span></span>

  <span data-ttu-id="82c95-179">调试配置建立后，可以在“调试”视图工具栏中的调试配置下拉列表中选择要在调试会话中使用的配置。</span><span class="sxs-lookup"><span data-stu-id="82c95-179">Once the debug configuration is established, you can select which configuration you want to use during a debug session by selecting one from the debug configuration drop-down in the **Debug** view's toolbar.</span></span>

<span data-ttu-id="82c95-180">以下博客提供有关将 PowerShell 扩展用于 Visual Studio Code 的有用入门帮助：</span><span class="sxs-lookup"><span data-stu-id="82c95-180">There are a few blogs that may be helpful to get you started using PowerShell extension for Visual Studio Code:</span></span>

- <span data-ttu-id="82c95-181">[PowerShell 扩展插件][ps-extension]</span><span class="sxs-lookup"><span data-stu-id="82c95-181">[PowerShell Extension][ps-extension]</span></span>
- <span data-ttu-id="82c95-182">[在 Visual Studio Code 中编写和调试 PowerShell 脚本][debug]</span><span class="sxs-lookup"><span data-stu-id="82c95-182">[Write and debug PowerShell scripts in Visual Studio Code][debug]</span></span>
- <span data-ttu-id="82c95-183">[Visual Studio Code 调试指南][vscode-guide]</span><span class="sxs-lookup"><span data-stu-id="82c95-183">[Debugging Visual Studio Code Guidance][vscode-guide]</span></span>
- <span data-ttu-id="82c95-184">[在 Visual Studio Code 中调试 PowerShell][ps-vscode]</span><span class="sxs-lookup"><span data-stu-id="82c95-184">[Debugging PowerShell in Visual Studio Code][ps-vscode]</span></span>
- <span data-ttu-id="82c95-185">[在 Visual Studio Code 中进行 PowerShell 开发][getting-started]</span><span class="sxs-lookup"><span data-stu-id="82c95-185">[Get started with PowerShell development in Visual Studio Code][getting-started]</span></span>
- <span data-ttu-id="82c95-186">[适用于 PowerShell 开发的 Visual Studio Code 编辑功能 – 第 1 部分][editing-part1]</span><span class="sxs-lookup"><span data-stu-id="82c95-186">[Visual Studio Code editing features for PowerShell development – Part 1][editing-part1]</span></span>
- <span data-ttu-id="82c95-187">[适用于 PowerShell 开发的 Visual Studio Code 编辑功能 – 第 2 部分][editing-part2]</span><span class="sxs-lookup"><span data-stu-id="82c95-187">[Visual Studio Code editing features for PowerShell development – Part 2][editing-part2]</span></span>
- <span data-ttu-id="82c95-188">[在 Visual Studio Code 中调试 PowerShell 脚本 – 第 1 部分][debugging-part1]</span><span class="sxs-lookup"><span data-stu-id="82c95-188">[Debugging PowerShell script in Visual Studio Code – Part 1][debugging-part1]</span></span>
- <span data-ttu-id="82c95-189">[在 Visual Studio Code 中调试 PowerShell 脚本 – 第 2 部分][debugging-part2]</span><span class="sxs-lookup"><span data-stu-id="82c95-189">[Debugging PowerShell script in Visual Studio Code – Part 2][debugging-part2]</span></span>

[ise]: ../ise/Introducing-the-Windows-PowerShell-ISE.md
[install-pscore-linux]:  ../../setup/Installing-PowerShell-Core-on-Linux.md
[install-pscore-macos]:  ../../setup/Installing-PowerShell-Core-on-macOS.md
[install-pscore-windows]: ../../setup/Installing-PowerShell-Core-on-Windows.md
[install-winps]: ../../setup/Installing-Windows-PowerShell.md
[ps-extension]: https://blogs.msdn.microsoft.com/cdndevs/2015/12/11/visual-studio-code-powershell-extension/
[debug]: https://blogs.msdn.microsoft.com/powershell/2015/11/16/announcing-powershell-language-support-for-visual-studio-code-and-more/
[vscode-guide]: https://johnpapa.net/debugging-with-visual-studio-code/
[ps-vscode]: https://github.com/PowerShell/vscode-powershell/tree/master/examples
[getting-started]: https://blogs.technet.microsoft.com/heyscriptingguy/2016/12/05/get-started-with-powershell-development-in-visual-studio-code/
[editing-part1]: https://blogs.technet.microsoft.com/heyscriptingguy/2017/01/11/visual-studio-code-editing-features-for-powershell-development-part-1/
[editing-part2]: https://blogs.technet.microsoft.com/heyscriptingguy/2017/01/12/visual-studio-code-editing-features-for-powershell-development-part-2/
[debugging-part1]: https://blogs.technet.microsoft.com/heyscriptingguy/2017/02/06/debugging-powershell-script-in-visual-studio-code-part-1/
[debugging-part2]: https://blogs.technet.microsoft.com/heyscriptingguy/2017/02/13/debugging-powershell-script-in-visual-studio-code-part-2/

## <a name="powershell-extension-for-visual-studio-code"></a><span data-ttu-id="82c95-190">适用于 Visual Studio Code 的 PowerShell 扩展</span><span class="sxs-lookup"><span data-stu-id="82c95-190">PowerShell Extension for Visual Studio Code</span></span>

<span data-ttu-id="82c95-191">可以在 [GitHub](https://github.com/PowerShell/vscode-powershell) 上找到 PowerShell 扩展的源代码。</span><span class="sxs-lookup"><span data-stu-id="82c95-191">The PowerShell extension's source code can be found on [GitHub](https://github.com/PowerShell/vscode-powershell).</span></span>