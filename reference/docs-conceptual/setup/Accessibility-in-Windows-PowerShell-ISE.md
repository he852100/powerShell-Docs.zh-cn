---
ms.date: 2017-06-05
keywords: powershell,cmdlet
title: "Windows PowerShell ISE 中的辅助功能"
ms.assetid: a078f9d1-dd6b-4323-b16d-0622cd993aa8
ms.openlocfilehash: 1231271067f32ff888504344bc324b13aade9c33
ms.sourcegitcommit: 598b7835046577841aea2211d613bb8513271a8b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/08/2017
---
# <a name="accessibility-in-windows-powershell-ise"></a><span data-ttu-id="7f1ae-103">Windows PowerShell ISE 中的辅助功能</span><span class="sxs-lookup"><span data-stu-id="7f1ae-103">Accessibility in Windows PowerShell ISE</span></span>
<span data-ttu-id="7f1ae-104">本主题介绍 Windows PowerShell® 集成脚本环境 (ISE) 的辅助功能，也许对你有所帮助。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-104">This topic describes the accessibility features of Windows PowerShell® Integrated Scripting Environment (ISE) that you might find helpful.</span></span>

* [<span data-ttu-id="7f1ae-105">如何更改控制台和脚本窗格的大小和位置</span><span class="sxs-lookup"><span data-stu-id="7f1ae-105">How to change the size and location of the Console and Script Panes</span></span>](#bkmk_1)
* [<span data-ttu-id="7f1ae-106">编辑文本的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-106">Keyboard shortcuts for editing text</span></span>](#bkmk_2)
* [<span data-ttu-id="7f1ae-107">运行脚本的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-107">Keyboard shortcuts for running scripts</span></span>](#bkmk_3)
* [<span data-ttu-id="7f1ae-108">自定义视图的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-108">Keyboard shortcuts for customizing the view</span></span>](#bkmk_4)
* [<span data-ttu-id="7f1ae-109">调试脚本的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-109">Keyboard shortcuts for debugging scripts</span></span>](#bkmk_5)
* [<span data-ttu-id="7f1ae-110">Windows PowerShell 选项卡的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-110">Keyboard shortcuts for Windows PowerShell tabs</span></span>](#bkmk_6)
* [<span data-ttu-id="7f1ae-111">启动和退出的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-111">Keyboard shortcuts for starting and exiting</span></span>](#bkmk_7)

<span data-ttu-id="7f1ae-112">Microsoft 致力于使其产品和服务更便于每个人使用。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-112">Microsoft is committed to making its products and services easier for everyone to use.</span></span> <span data-ttu-id="7f1ae-113">下列主题提供有关使 Windows PowerShell ISE 更便于残障人士访问的功能、产品和服务的信息。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-113">The following topics provide information about the features, products, and services that make Windows PowerShell ISE more accessible for people with disabilities.</span></span>

<span data-ttu-id="7f1ae-114">Windows PowerShell ISE 支持高对比度模式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-114">Windows PowerShell ISE supports high contrast mode.</span></span> <span data-ttu-id="7f1ae-115">为方便有视觉障碍的用户，通过用于管理断点的 cmdlet（例如 [Get-PSBreakpoint](https://technet.microsoft.com/en-us/library/0bf48936-00ab-411c-b5e0-9b10a812a3c6) 和 [Set-PSBreakpoint](https://technet.microsoft.com/en-us/library/6afd5d2c-a285-4796-8607-3cbf49471420)）提供断点信息。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-115">For the visually impaired, breakpoint information is available through the cmdlets for managing breakpoints, such as [Get-PSBreakpoint](https://technet.microsoft.com/en-us/library/0bf48936-00ab-411c-b5e0-9b10a812a3c6) and [Set-PSBreakpoint](https://technet.microsoft.com/en-us/library/6afd5d2c-a285-4796-8607-3cbf49471420).</span></span> <span data-ttu-id="7f1ae-116">有关详细信息，请参阅[如何在 Windows PowerShell ISE 中调试脚本](../core-powershell/ise/How-to-Debug-Scripts-in-Windows-PowerShell-ISE.md#bkmk_1)中的“如何管理断点”。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-116">For more information please see “How to manage breakpoints” in [How to Debug Scripts in the Windows PowerShell ISE](../core-powershell/ise/How-to-Debug-Scripts-in-Windows-PowerShell-ISE.md#bkmk_1).</span></span> <span data-ttu-id="7f1ae-117">除了 Microsoft Windows 中的辅助功能和实用工具外，以下功能也能使残障人士更轻松地访问 Windows PowerShell ISE：</span><span class="sxs-lookup"><span data-stu-id="7f1ae-117">In addition to accessibility features and utilities in Microsoft Windows, the following features make Windows PowerShell ISE more accessible for people with disabilities:</span></span>

-   <span data-ttu-id="7f1ae-118">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-118">Keyboard Shortcuts</span></span>

-   <span data-ttu-id="7f1ae-119">语法着色表和使用 [$psISE.Options](https://technet.microsoft.com/en-us/library/75e2a76f-f3d1-490b-ad5d-e3829946aabb) 脚本对象修改多个其他颜色设置的能力。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-119">Syntax Coloring Table and the ability to modify several other color settings using the [$psISE.Options](https://technet.microsoft.com/en-us/library/75e2a76f-f3d1-490b-ad5d-e3829946aabb) scripting object.</span></span>

-   <span data-ttu-id="7f1ae-120">文字大小更改</span><span class="sxs-lookup"><span data-stu-id="7f1ae-120">Text Size Change</span></span>

## <span data-ttu-id="7f1ae-121"><a name="bkmk_1"></a>如何更改控制台和脚本窗格的大小和位置</span><span class="sxs-lookup"><span data-stu-id="7f1ae-121"><a name="bkmk_1"></a>How to change the size and location of the Console and Script Panes</span></span>
<span data-ttu-id="7f1ae-122">可以使用以下步骤更改控制台窗格和脚本窗格的大小和位置。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-122">You can use the following steps to change the size and location of the Console Pane and the Script Pane.</span></span> <span data-ttu-id="7f1ae-123">再次打开 Windows PowerShell ISE 时，将会保留你对大小和位置所做的更改。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-123">When you open the Windows PowerShell ISE again, the size and location changes you made will be retained.</span></span>

### <a name="to-resize-the-script-pane-and-console-pane"></a><span data-ttu-id="7f1ae-124">调整脚本窗格和控制台窗格的大小</span><span class="sxs-lookup"><span data-stu-id="7f1ae-124">To resize the Script Pane and Console Pane</span></span>

1.  <span data-ttu-id="7f1ae-125">将鼠标指针放在脚本窗格和控制台窗格之间的拆分行上。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-125">Pause the pointer on the split line between the Script Pane and Console Pane.</span></span>

2.  <span data-ttu-id="7f1ae-126">当鼠标指针更改为双向箭头时，拖动边框来更改窗格的大小。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-126">When the mouse pointer changes to a two-headed arrow, drag the border to change the size of the pane.</span></span>

### <a name="to-move-the-script-pane-and-console-pane"></a><span data-ttu-id="7f1ae-127">移动脚本窗格和控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-127">To move the Script Pane and Console Pane</span></span>
<span data-ttu-id="7f1ae-128">执行下列操作之一：</span><span class="sxs-lookup"><span data-stu-id="7f1ae-128">Do one of the following:</span></span>

-   <span data-ttu-id="7f1ae-129">若要将脚本窗格移动到控制台窗格上方，请按 **CTRL+1**，或单击工具栏上的“**顶部显示脚本窗格**”图标，或单击“**视图**”菜单上的“**顶部显示脚本窗格**”。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-129">To move the Script Pane above the Console Pane, press **CTRL+1** or, on the toolbar, click the **Show Script Pane Top** icon, or in the **View** menu, click **Show Script Pane Top**.</span></span>

-   <span data-ttu-id="7f1ae-130">若要将脚本窗格移动到控制台窗格的右侧，请按 **CTRL+2**，或单击工具栏上的“**显示脚本窗格右侧**”图标，或单击“**视图**”菜单上的“**显示脚本窗格右侧**”。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-130">To move the Script Pane to the right of the Console Pane, press **CTRL+2** or, on the toolbar, click the **Show Script Pane Right** icon, or in the **View** menu, click **Show Script Pane Right**.</span></span>

-   <span data-ttu-id="7f1ae-131">若要最大化脚本窗格，请按 **CTRL+3**，或单击工具栏上的“**显示最大化脚本窗格**”图标，或单击“**视图**”菜单上的“**显示最大化脚本窗格**”。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-131">To maximize the Script Pane, press **CTRL+3** or, on the toolbar, click the **Show Script Pane Maximized** icon, or in the **View** menu, click **Show Script Pane Maximized**.</span></span>

-   <span data-ttu-id="7f1ae-132">若要最大化控制台窗格并隐藏脚本窗格，请在选项卡行的最右侧边缘上单击“隐藏脚本窗格”图标，在“视图”菜单上单击以取消选择“显示脚本窗格”菜单选项。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-132">To maximize the Console Pane and hide the Script Pane, on the far right edge of the row of tabs, click the **Hide Script Pane** icon, in the **View** menu, click to deselect the **Show Script Pane** menu option.</span></span>

-   <span data-ttu-id="7f1ae-133">若要在控制台窗格最大化时显示脚本窗格，请在选项卡行的最右侧边缘上单击“隐藏脚本窗格”图标，或在“视图”菜单上单击以选择“显示脚本窗格”菜单选项。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-133">To display the Script Pane when the Console Pane is maximized, on the far right edge of the row of tabs, click the **Show Script Pane** icon, or in the **View** menu, click to select the **Show Script Pane** menu option.</span></span>

## <span data-ttu-id="7f1ae-134"><a name="bkmk_2"></a>编辑文本的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-134"><a name="bkmk_2"></a>Keyboard shortcuts for editing text</span></span>
<span data-ttu-id="7f1ae-135">编辑文本时可以使用以下键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-135">You can use the following keyboard shortcuts when you edit text.</span></span>

|<span data-ttu-id="7f1ae-136">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-136">Action</span></span>|<span data-ttu-id="7f1ae-137">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-137">Keyboard Shortcuts</span></span>|<span data-ttu-id="7f1ae-138">用于</span><span class="sxs-lookup"><span data-stu-id="7f1ae-138">Use in</span></span>|
|----------|----------------------|----------|
|<span data-ttu-id="7f1ae-139">**复制**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-139">**Copy**</span></span>|<span data-ttu-id="7f1ae-140">CTRL+C</span><span class="sxs-lookup"><span data-stu-id="7f1ae-140">CTRL+C</span></span>|<span data-ttu-id="7f1ae-141">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-141">Script Pane, Console Pane</span></span>|
|<span data-ttu-id="7f1ae-142">**剪切**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-142">**Cut**</span></span>|<span data-ttu-id="7f1ae-143">CTRL+X</span><span class="sxs-lookup"><span data-stu-id="7f1ae-143">CTRL+X</span></span>|<span data-ttu-id="7f1ae-144">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-144">Script Pane, Console Pane</span></span>|
|<span data-ttu-id="7f1ae-145">**在脚本中查找**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-145">**Find in Script**</span></span>|<span data-ttu-id="7f1ae-146">Ctrl+F</span><span class="sxs-lookup"><span data-stu-id="7f1ae-146">CTRL+F</span></span>|<span data-ttu-id="7f1ae-147">脚本窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-147">Script Pane</span></span>|
|<span data-ttu-id="7f1ae-148">**在脚本中查找下一个**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-148">**Find Next in Script**</span></span>|<span data-ttu-id="7f1ae-149">F3</span><span class="sxs-lookup"><span data-stu-id="7f1ae-149">F3</span></span>|<span data-ttu-id="7f1ae-150">脚本窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-150">Script Pane</span></span>|
|<span data-ttu-id="7f1ae-151">**在脚本中查找上一个**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-151">**Find Previous in Script**</span></span>|<span data-ttu-id="7f1ae-152">SHIFT+F3</span><span class="sxs-lookup"><span data-stu-id="7f1ae-152">SHIFT+F3</span></span>|<span data-ttu-id="7f1ae-153">脚本窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-153">Script Pane</span></span>|
|<span data-ttu-id="7f1ae-154">**粘贴**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-154">**Paste**</span></span>|<span data-ttu-id="7f1ae-155">CTRL+V</span><span class="sxs-lookup"><span data-stu-id="7f1ae-155">CTRL+V</span></span>|<span data-ttu-id="7f1ae-156">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-156">Script Pane, Console Pane</span></span>|
|<span data-ttu-id="7f1ae-157">**重做**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-157">**Redo**</span></span>|<span data-ttu-id="7f1ae-158">CTRL+Y</span><span class="sxs-lookup"><span data-stu-id="7f1ae-158">CTRL+Y</span></span>|<span data-ttu-id="7f1ae-159">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-159">Script Pane, Console Pane</span></span>|
|<span data-ttu-id="7f1ae-160">**在脚本中替换**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-160">**Replace in Script**</span></span>|<span data-ttu-id="7f1ae-161">CTRL+H</span><span class="sxs-lookup"><span data-stu-id="7f1ae-161">CTRL+H</span></span>|<span data-ttu-id="7f1ae-162">脚本窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-162">Script Pane</span></span>|
|<span data-ttu-id="7f1ae-163">**保存**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-163">**Save**</span></span>|<span data-ttu-id="7f1ae-164">Ctrl+S</span><span class="sxs-lookup"><span data-stu-id="7f1ae-164">CTRL+S</span></span>|<span data-ttu-id="7f1ae-165">脚本窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-165">Script Pane</span></span>|
|<span data-ttu-id="7f1ae-166">**全选**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-166">**Select All**</span></span>|<span data-ttu-id="7f1ae-167">CTRL+A</span><span class="sxs-lookup"><span data-stu-id="7f1ae-167">CTRL+A</span></span>|<span data-ttu-id="7f1ae-168">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-168">Script Pane, Console Pane</span></span>|
|<span data-ttu-id="7f1ae-169">**撤消**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-169">**Undo**</span></span>|<span data-ttu-id="7f1ae-170">CTRL+Z</span><span class="sxs-lookup"><span data-stu-id="7f1ae-170">CTRL+Z</span></span>|<span data-ttu-id="7f1ae-171">脚本窗格、控制台窗格</span><span class="sxs-lookup"><span data-stu-id="7f1ae-171">Script Pane, Console Pane</span></span>|

## <span data-ttu-id="7f1ae-172"><a name="bkmk_3"></a>运行脚本的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-172"><a name="bkmk_3"></a>Keyboard shortcuts for running scripts</span></span>
<span data-ttu-id="7f1ae-173">在脚本窗格中运行脚本时，可使用以下键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-173">You can use the following keyboard shortcuts when you run scripts in the Script Pane.</span></span>

|<span data-ttu-id="7f1ae-174">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-174">Action</span></span>|<span data-ttu-id="7f1ae-175">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-175">Keyboard Shortcut</span></span>|
|----------|---------------------|
|<span data-ttu-id="7f1ae-176">**新建**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-176">**New**</span></span>|<span data-ttu-id="7f1ae-177">Ctrl+N</span><span class="sxs-lookup"><span data-stu-id="7f1ae-177">CTRL+N</span></span>|
|<span data-ttu-id="7f1ae-178">**打开**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-178">**Open**</span></span>|<span data-ttu-id="7f1ae-179">Ctrl+O</span><span class="sxs-lookup"><span data-stu-id="7f1ae-179">CTRL+O</span></span>|
|<span data-ttu-id="7f1ae-180">**运行**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-180">**Run**</span></span>|<span data-ttu-id="7f1ae-181">F5</span><span class="sxs-lookup"><span data-stu-id="7f1ae-181">F5</span></span>|
|<span data-ttu-id="7f1ae-182">**运行选定内容**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-182">**Run Selection**</span></span>|<span data-ttu-id="7f1ae-183">F8</span><span class="sxs-lookup"><span data-stu-id="7f1ae-183">F8</span></span>|
|<span data-ttu-id="7f1ae-184">**停止执行**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-184">**Stop Execution**</span></span>|<span data-ttu-id="7f1ae-185">CTRL+BREAK。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-185">CTRL+BREAK.</span></span> <span data-ttu-id="7f1ae-186">可以在上下文不明确时（未选定任何文本时）使用 CTRL+C。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-186">CTRL+C can be used when the context is unambiguous (when there is no text selected).</span></span>|
|<span data-ttu-id="7f1ae-187">**Tab**（切换到下一个脚本）</span><span class="sxs-lookup"><span data-stu-id="7f1ae-187">**Tab** (to next script)</span></span>|<span data-ttu-id="7f1ae-188">CTRL+TAB **注意：**仅当打开单个 PowerShell 选项卡时，或打开多个 PowerShell 选项卡而焦点位于脚本窗格中时，切换到下一个脚本才有效。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-188">CTRL+TAB **Note:** Tab to next script works only when you have a single PowerShell tab open, or when you have more than one PowerShell tab open, but the focus is in the Script Pane.</span></span>|
|<span data-ttu-id="7f1ae-189">**Tab**（切换到上一个脚本）</span><span class="sxs-lookup"><span data-stu-id="7f1ae-189">**Tab** (to previous script)</span></span>|<span data-ttu-id="7f1ae-190">CTRL+SHIFT+TAB **注意：**仅当打开单个 PowerShell 选项卡时，或打开多个 PowerShell 选项卡而焦点位于脚本窗格中时，切换到上一个脚本才有效。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-190">CTRL+SHIFT+TAB **Note:** Tab to previous script works when you have only one PowerShell tab open, or if you have more  than one PowerShell tab open, and the focus is in the Script Pane.</span></span>|

## <span data-ttu-id="7f1ae-191"><a name="bkmk_4"></a>自定义视图的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-191"><a name="bkmk_4"></a>Keyboard shortcuts for customizing the view</span></span>
<span data-ttu-id="7f1ae-192">可以使用以下键盘快捷方式在 Windows PowerShell ISE 中自定义视图。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-192">You can use the following keyboard shortcuts to customize the view in Windows PowerShell ISE.</span></span> <span data-ttu-id="7f1ae-193">可从应用程序中的所有窗格对它们进行访问。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-193">They are accessible from all the panes in the application.</span></span>

|<span data-ttu-id="7f1ae-194">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-194">Action</span></span>|<span data-ttu-id="7f1ae-195">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-195">Keyboard Shortcut</span></span>|
|----------|---------------------|
|<span data-ttu-id="7f1ae-196">**转到控制台窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-196">**Go to Console Pane**</span></span>|<span data-ttu-id="7f1ae-197">CTRL+D</span><span class="sxs-lookup"><span data-stu-id="7f1ae-197">CTRL+D</span></span>|
|<span data-ttu-id="7f1ae-198">**转到脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-198">**Go to Script Pane**</span></span>|<span data-ttu-id="7f1ae-199">CTRL+I</span><span class="sxs-lookup"><span data-stu-id="7f1ae-199">CTRL+I</span></span>|
|<span data-ttu-id="7f1ae-200">**显示脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-200">**Show Script Pane**</span></span>|<span data-ttu-id="7f1ae-201">CTRL+R</span><span class="sxs-lookup"><span data-stu-id="7f1ae-201">CTRL+R</span></span>|
|<span data-ttu-id="7f1ae-202">**隐藏脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-202">**Hide Script Pane**</span></span>|<span data-ttu-id="7f1ae-203">CTRL+R</span><span class="sxs-lookup"><span data-stu-id="7f1ae-203">CTRL+R</span></span>|
||
|<span data-ttu-id="7f1ae-204">**向上移动脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-204">**Move Script Pane Up**</span></span>|<span data-ttu-id="7f1ae-205">CTRL+1</span><span class="sxs-lookup"><span data-stu-id="7f1ae-205">CTRL+1</span></span>|
|<span data-ttu-id="7f1ae-206">**向右移动脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-206">**Move Script Pane Right**</span></span>|<span data-ttu-id="7f1ae-207">CTRL+2</span><span class="sxs-lookup"><span data-stu-id="7f1ae-207">CTRL+2</span></span>|
|<span data-ttu-id="7f1ae-208">**最大化脚本窗格**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-208">**Maximize Script Pane**</span></span>|<span data-ttu-id="7f1ae-209">CTRL+3</span><span class="sxs-lookup"><span data-stu-id="7f1ae-209">CTRL+3</span></span>|
|<span data-ttu-id="7f1ae-210">**放大**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-210">**Zoom In**</span></span>|<span data-ttu-id="7f1ae-211">CTRL+加号</span><span class="sxs-lookup"><span data-stu-id="7f1ae-211">CTRL+PLUS SIGN</span></span>|
|<span data-ttu-id="7f1ae-212">**缩小**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-212">**Zoom Out**</span></span>|<span data-ttu-id="7f1ae-213">CTRL+减号</span><span class="sxs-lookup"><span data-stu-id="7f1ae-213">CTRL+MINUS SIGN</span></span>|

## <span data-ttu-id="7f1ae-214"><a name="bkmk_5"></a></span><span class="sxs-lookup"><span data-stu-id="7f1ae-214"><a name="bkmk_5"></a>Keyboard shortcuts for debugging scripts</span></span>
<span data-ttu-id="7f1ae-215">调试脚本时，可使用以下键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-215">You can use the following keyboard shortcuts when you debug scripts.</span></span>

|<span data-ttu-id="7f1ae-216">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-216">Action</span></span>|<span data-ttu-id="7f1ae-217">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-217">Keyboard Shortcut</span></span>|<span data-ttu-id="7f1ae-218">用于</span><span class="sxs-lookup"><span data-stu-id="7f1ae-218">Use in</span></span>|
|----------|---------------------|----------|
|<span data-ttu-id="7f1ae-219">**运行/继续**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-219">**Run/Continue**</span></span>|<span data-ttu-id="7f1ae-220">F5</span><span class="sxs-lookup"><span data-stu-id="7f1ae-220">F5</span></span>|<span data-ttu-id="7f1ae-221">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-221">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-222">**步入**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-222">**Step Into**</span></span>|<span data-ttu-id="7f1ae-223">F11</span><span class="sxs-lookup"><span data-stu-id="7f1ae-223">F11</span></span>|<span data-ttu-id="7f1ae-224">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-224">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-225">**步越**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-225">**Step Over**</span></span>|<span data-ttu-id="7f1ae-226">F10</span><span class="sxs-lookup"><span data-stu-id="7f1ae-226">F10</span></span>|<span data-ttu-id="7f1ae-227">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-227">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-228">**步出**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-228">**Step Out**</span></span>|<span data-ttu-id="7f1ae-229">SHIFT+F11</span><span class="sxs-lookup"><span data-stu-id="7f1ae-229">SHIFT+F11</span></span>|<span data-ttu-id="7f1ae-230">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-230">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-231">**显示调用堆栈**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-231">**Display Call Stack**</span></span>|<span data-ttu-id="7f1ae-232">CTRL+SHIFT+D</span><span class="sxs-lookup"><span data-stu-id="7f1ae-232">CTRL+SHIFT+D</span></span>|<span data-ttu-id="7f1ae-233">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-233">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-234">**列出断点**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-234">**List Breakpoints**</span></span>|<span data-ttu-id="7f1ae-235">CTRL+SHIFT+L</span><span class="sxs-lookup"><span data-stu-id="7f1ae-235">CTRL+SHIFT+L</span></span>|<span data-ttu-id="7f1ae-236">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-236">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-237">**切换断点**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-237">**Toggle Breakpoint**</span></span>|<span data-ttu-id="7f1ae-238">F9</span><span class="sxs-lookup"><span data-stu-id="7f1ae-238">F9</span></span>|<span data-ttu-id="7f1ae-239">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-239">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-240">**移除所有断点**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-240">**Remove All Breakpoints**</span></span>|<span data-ttu-id="7f1ae-241">CTRL+SHIFT+F9</span><span class="sxs-lookup"><span data-stu-id="7f1ae-241">CTRL+SHIFT+F9</span></span>|<span data-ttu-id="7f1ae-242">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-242">Script Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-243">**停止调试器**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-243">**Stop Debugger**</span></span>|<span data-ttu-id="7f1ae-244">SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="7f1ae-244">SHIFT+F5</span></span>|<span data-ttu-id="7f1ae-245">脚本窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-245">Script Pane, when debugging a script</span></span>|

> [!NOTE]
> <span data-ttu-id="7f1ae-246">在 Windows PowerShell ISE 中调试脚本时，也可以使用为 Windows PowerShell 控制台而设计的键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-246">You can also use the keyboard shortcuts designed for the Windows PowerShell console when you debug scripts in Windows PowerShell ISE.</span></span> <span data-ttu-id="7f1ae-247">若要使用这些快捷方式，必须在控制台窗格中输入该快捷方式并按 ENTER。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-247">To use these shortcuts, you must type the shortcut in the Console Pane and press ENTER.</span></span>

|<span data-ttu-id="7f1ae-248">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-248">Action</span></span>|<span data-ttu-id="7f1ae-249">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-249">Keyboard Shortcut</span></span>|<span data-ttu-id="7f1ae-250">用于</span><span class="sxs-lookup"><span data-stu-id="7f1ae-250">Use in</span></span>|
|----------|---------------------|----------|
|<span data-ttu-id="7f1ae-251">**继续**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-251">**Continue**</span></span>|<span data-ttu-id="7f1ae-252">C</span><span class="sxs-lookup"><span data-stu-id="7f1ae-252">C</span></span>|<span data-ttu-id="7f1ae-253">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-253">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-254">**步入**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-254">**Step Into**</span></span>|<span data-ttu-id="7f1ae-255">S</span><span class="sxs-lookup"><span data-stu-id="7f1ae-255">S</span></span>|<span data-ttu-id="7f1ae-256">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-256">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-257">**步越**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-257">**Step Over**</span></span>|<span data-ttu-id="7f1ae-258">V</span><span class="sxs-lookup"><span data-stu-id="7f1ae-258">V</span></span>|<span data-ttu-id="7f1ae-259">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-259">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-260">**步出**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-260">**Step Out**</span></span>|<span data-ttu-id="7f1ae-261">O</span><span class="sxs-lookup"><span data-stu-id="7f1ae-261">O</span></span>|<span data-ttu-id="7f1ae-262">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-262">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-263">重复上一命令（用于步入或步越）</span><span class="sxs-lookup"><span data-stu-id="7f1ae-263">**Repeat Last Command** (for Step Into or Step Over)</span></span>|<span data-ttu-id="7f1ae-264">Enter</span><span class="sxs-lookup"><span data-stu-id="7f1ae-264">ENTER</span></span>|<span data-ttu-id="7f1ae-265">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-265">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-266">**显示调用堆栈**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-266">**Display Call Stack**</span></span>|<span data-ttu-id="7f1ae-267">K</span><span class="sxs-lookup"><span data-stu-id="7f1ae-267">K</span></span>|<span data-ttu-id="7f1ae-268">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-268">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-269">**停止调试**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-269">**Stop Debugging**</span></span>|<span data-ttu-id="7f1ae-270">Q</span><span class="sxs-lookup"><span data-stu-id="7f1ae-270">Q</span></span>|<span data-ttu-id="7f1ae-271">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-271">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-272">**列出脚本**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-272">**List the Script**</span></span>|<span data-ttu-id="7f1ae-273">L</span><span class="sxs-lookup"><span data-stu-id="7f1ae-273">L</span></span>|<span data-ttu-id="7f1ae-274">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-274">Console Pane, when debugging a script</span></span>|
|<span data-ttu-id="7f1ae-275">**显示控制台调试命令**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-275">**Display Console Debugging Commands**</span></span>|<span data-ttu-id="7f1ae-276">H 或 ?</span><span class="sxs-lookup"><span data-stu-id="7f1ae-276">H or ?</span></span>|<span data-ttu-id="7f1ae-277">控制台窗格，调试脚本时</span><span class="sxs-lookup"><span data-stu-id="7f1ae-277">Console Pane, when debugging a script</span></span>|

## <span data-ttu-id="7f1ae-278"><a name="bkmk_6"></a>Windows PowerShell 选项卡的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-278"><a name="bkmk_6"></a>Keyboard shortcuts for Windows PowerShell tabs</span></span>
<span data-ttu-id="7f1ae-279">使用 Windows PowerShell 选项卡时，可使用以下键盘快捷方式。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-279">You can use the following keyboard shortcuts when you use Windows PowerShell tabs.</span></span>

|<span data-ttu-id="7f1ae-280">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-280">Action</span></span>|<span data-ttu-id="7f1ae-281">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-281">Keyboard Shortcut</span></span>|
|----------|---------------------|
|<span data-ttu-id="7f1ae-282">**关闭 PowerShell 选项卡**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-282">**Close PowerShell Tab**</span></span>|<span data-ttu-id="7f1ae-283">Ctrl+W</span><span class="sxs-lookup"><span data-stu-id="7f1ae-283">CTRL+W</span></span>|
|<span data-ttu-id="7f1ae-284">**新建 PowerShell 选项卡**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-284">**New PowerShell Tab**</span></span>|<span data-ttu-id="7f1ae-285">CTRL+T</span><span class="sxs-lookup"><span data-stu-id="7f1ae-285">CTRL+T</span></span>|
|<span data-ttu-id="7f1ae-286">**上一个 PowerShell 选项卡**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-286">**Previous PowerShell tab**</span></span>|<span data-ttu-id="7f1ae-287">CTRL+SHIFT+TAB。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-287">CTRL+SHIFT+TAB.</span></span> <span data-ttu-id="7f1ae-288">此快捷方式仅在任意 PowerShell 选项卡上都未打开任何文件时起作用。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-288">This shortcut works only when no files are open on any PowerShell tab.</span></span>|
|<span data-ttu-id="7f1ae-289">**下一个 Windows PowerShell 选项卡**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-289">**Next Windows PowerShell tab**</span></span>|<span data-ttu-id="7f1ae-290">CTRL+TAB。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-290">CTRL+TAB.</span></span> <span data-ttu-id="7f1ae-291">此快捷方式仅在任意 PowerShell 选项卡上都未打开任何文件时起作用。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-291">This shortcut works only when no files are open on any PowerShell tab.</span></span>|

## <span data-ttu-id="7f1ae-292"><a name="bkmk_7"></a>启动和退出的键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-292"><a name="bkmk_7"></a>Keyboard shortcuts for starting and exiting</span></span>
<span data-ttu-id="7f1ae-293">可以使用以下键盘快捷方式来启动 Windows PowerShell 控制台 (PowerShell.exe) 或退出 Windows PowerShell ISE。</span><span class="sxs-lookup"><span data-stu-id="7f1ae-293">You can use the following keyboard shortcuts to start the Windows PowerShell console (PowerShell.exe) or to exit Windows PowerShell ISE.</span></span>

|<span data-ttu-id="7f1ae-294">操作</span><span class="sxs-lookup"><span data-stu-id="7f1ae-294">Action</span></span>|<span data-ttu-id="7f1ae-295">键盘快捷方式</span><span class="sxs-lookup"><span data-stu-id="7f1ae-295">Keyboard Shortcut</span></span>|
|----------|---------------------|
|<span data-ttu-id="7f1ae-296">**退出**</span><span class="sxs-lookup"><span data-stu-id="7f1ae-296">**Exit**</span></span>|<span data-ttu-id="7f1ae-297">Alt + F4</span><span class="sxs-lookup"><span data-stu-id="7f1ae-297">ALT+F4</span></span>|
|<span data-ttu-id="7f1ae-298">**启动 PowerShell.exe**（Windows PowerShell 控制台）</span><span class="sxs-lookup"><span data-stu-id="7f1ae-298">**Start PowerShell.exe** (Windows PowerShell console)</span></span>|<span data-ttu-id="7f1ae-299">CTRL+SHIFT+P</span><span class="sxs-lookup"><span data-stu-id="7f1ae-299">CTRL+SHIFT+P</span></span>|

## <a name="see-also"></a><span data-ttu-id="7f1ae-300">另请参阅</span><span class="sxs-lookup"><span data-stu-id="7f1ae-300">See Also</span></span>
- [<span data-ttu-id="7f1ae-301">使用 Windows PowerShell ISE</span><span class="sxs-lookup"><span data-stu-id="7f1ae-301">Using the Windows PowerShell ISE</span></span>](../core-powershell/ise/Using-the-Windows-PowerShell-ISE.md)
