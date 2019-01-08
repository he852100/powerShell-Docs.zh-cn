---
ms.date: 06/05/2017
keywords: powershell,cmdlet
title: ISEFileCollection 对象
ms.assetid: 0f86a427-ea38-4bce-85f8-06c98d30d508
ms.openlocfilehash: eb4b2784820cbe51f662fd2fd945d8760ef9dbff
ms.sourcegitcommit: 00ff76d7d9414fe585c04740b739b9cf14d711e1
ms.translationtype: MTE95
ms.contentlocale: zh-CN
ms.lasthandoff: 12/14/2018
ms.locfileid: "53401099"
---
# <a name="the-isefilecollection-object"></a><span data-ttu-id="00ad8-103">ISEFileCollection 对象</span><span class="sxs-lookup"><span data-stu-id="00ad8-103">The ISEFileCollection Object</span></span>

<span data-ttu-id="00ad8-104">**ISEFileCollection** 对象是 **ISEFile** 对象的集合。</span><span class="sxs-lookup"><span data-stu-id="00ad8-104">The **ISEFileCollection** object is a collection of **ISEFile** objects.</span></span> <span data-ttu-id="00ad8-105">例如，$psISE.CurrentPowerShellTab.Files 集合。</span><span class="sxs-lookup"><span data-stu-id="00ad8-105">An example is the $psISE.CurrentPowerShellTab.Files collection.</span></span>

## <a name="methods"></a><span data-ttu-id="00ad8-106">方法</span><span class="sxs-lookup"><span data-stu-id="00ad8-106">Methods</span></span>

### <a name="add-fullpath-"></a><span data-ttu-id="00ad8-107">Add\( \[fullPath\] \)</span><span class="sxs-lookup"><span data-stu-id="00ad8-107">Add\( \[fullPath\] \)</span></span>

<span data-ttu-id="00ad8-108">在 Windows PowerShell ISE 2.0 和更高版本中受支持。</span><span class="sxs-lookup"><span data-stu-id="00ad8-108">Supported in Windows PowerShell ISE 2.0 and later.</span></span>

<span data-ttu-id="00ad8-109">创建并返回一个新的未命名文件，并将其添加到集合中。</span><span class="sxs-lookup"><span data-stu-id="00ad8-109">Creates and returns a new untitled file and adds it to the collection.</span></span> <span data-ttu-id="00ad8-110">新创建的文件的 **IsUntitled** 属性为 **$true**。</span><span class="sxs-lookup"><span data-stu-id="00ad8-110">The **IsUntitled** property of the newly created file is **$true**.</span></span>

<span data-ttu-id="00ad8-111">**\[fullPath\]** - 可选字符串，表示文件的完全指定路径。</span><span class="sxs-lookup"><span data-stu-id="00ad8-111">**\[fullPath\]** - Optional string The fully specified path of the file.</span></span> <span data-ttu-id="00ad8-112">如果包含 **fullPath** 参数和相对路径，或者如果你使用文件名而不是完整路径，则会生成异常。</span><span class="sxs-lookup"><span data-stu-id="00ad8-112">An exception is generated if you include the **fullPath** parameter and a relative path, or if you use a file name instead of the full path.</span></span>

```powershell
# Adds a new untitled file to the collection of files in the current PowerShell tab.
$newFile = $psISE.CurrentPowerShellTab.Files.Add()

# Adds a file specified by its full path to the collection of files in the current PowerShell tab.
$psISE.CurrentPowerShellTab.Files.Add("$pshome\Examples\profile.ps1")
```

### <a name="remove-file-force-"></a><span data-ttu-id="00ad8-113">Remove\( File, \[Force\] \)</span><span class="sxs-lookup"><span data-stu-id="00ad8-113">Remove\( File, \[Force\] \)</span></span>

<span data-ttu-id="00ad8-114">在 Windows PowerShell ISE 2.0 和更高版本中受支持。</span><span class="sxs-lookup"><span data-stu-id="00ad8-114">Supported in Windows PowerShell ISE 2.0 and later.</span></span>

<span data-ttu-id="00ad8-115">从当前 PowerShell 选项卡中删除指定的文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-115">Removes a specified file from the current PowerShell tab.</span></span>

<span data-ttu-id="00ad8-116">**File** - 字符串，表示要从集合中删除的 ISEFile 文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-116">**File** - String The ISEFile file that you want to remove from the collection.</span></span> <span data-ttu-id="00ad8-117">如果尚未保存该文件，此方法将引发异常。</span><span class="sxs-lookup"><span data-stu-id="00ad8-117">If the file has not been saved, this method throws an exception.</span></span> <span data-ttu-id="00ad8-118">使用 **Force** 开关参数强制删除未保存的文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-118">Use the **Force** switch parameter to force the removal of an unsaved file.</span></span>

<span data-ttu-id="00ad8-119">**\[Force\]** - 可选布尔值，如果设置为 **$true**，即使在最后一次使用后尚未保存文件，也会授予权限来删除该文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-119">**\[Force\]** - optional Boolean If set to **$true**, grants permission to remove the file even if it has not been saved after last use.</span></span> <span data-ttu-id="00ad8-120">默认值为 **$false**。</span><span class="sxs-lookup"><span data-stu-id="00ad8-120">The default is **$false**.</span></span>

```powershell
# Removes the first opened file from the file collection associated with the current PowerShell tab.
# If the file has not yet been saved, then an exception is generated.
$firstfile = $psISE.CurrentPowerShellTab.Files[0]
$psISE.CurrentPowerShellTab.Files.Remove($firstfile)

# Removes the first opened file from the file collection associated with the current PowerShell tab, even if it has not been saved.
$firstfile = $psISE.CurrentPowerShellTab.Files[0]
$psISE.CurrentPowerShellTab.Files.Remove($firstfile, $true)
```

### <a name="setselectedfile-selectedfile-"></a><span data-ttu-id="00ad8-121">SetSelectedFile\( selectedFile \)</span><span class="sxs-lookup"><span data-stu-id="00ad8-121">SetSelectedFile\( selectedFile \)</span></span>

<span data-ttu-id="00ad8-122">在 Windows PowerShell ISE 2.0 和更高版本中受支持。</span><span class="sxs-lookup"><span data-stu-id="00ad8-122">Supported in Windows PowerShell ISE 2.0 and later.</span></span>

<span data-ttu-id="00ad8-123">选择由 **selectedFile** 参数指定的文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-123">Selects the file that is specified by the **selectedFile** parameter.</span></span>

<span data-ttu-id="00ad8-124">**selectedFile** - Microsoft.PowerShell.Host.ISE.ISEFile，要选择的 ISEFile 文件。</span><span class="sxs-lookup"><span data-stu-id="00ad8-124">**selectedFile** - Microsoft.PowerShell.Host.ISE.ISEFile The ISEFile file that you want to select.</span></span>

```powershell
# Selects the specified file.
$firstfile = $psISE.CurrentPowerShellTab.Files[0]
$psISE.CurrentPowerShellTab.Files.SetSelectedFile($firstfile)
```

## <a name="see-also"></a><span data-ttu-id="00ad8-125">另请参阅</span><span class="sxs-lookup"><span data-stu-id="00ad8-125">See Also</span></span>

- [<span data-ttu-id="00ad8-126">ISEFile 对象</span><span class="sxs-lookup"><span data-stu-id="00ad8-126">The ISEFile Object</span></span>](The-ISEFile-Object.md)
- [<span data-ttu-id="00ad8-127">Windows PowerShell ISE 脚本对象模型的用途</span><span class="sxs-lookup"><span data-stu-id="00ad8-127">Purpose of the Windows PowerShell ISE Scripting Object Model</span></span>](Purpose-of-the-Windows-PowerShell-ISE-Scripting-Object-Model.md)
- [<span data-ttu-id="00ad8-128">ISE 对象模型层次结构</span><span class="sxs-lookup"><span data-stu-id="00ad8-128">The ISE Object Model Hierarchy</span></span>](The-ISE-Object-Model-Hierarchy.md)