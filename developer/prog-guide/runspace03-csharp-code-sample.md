---
title: RunSpace03 (C#) 代码示例 |Microsoft Docs
ms.custom: ''
ms.date: 09/13/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9ac8ab99-1856-4d6f-b30d-c0a18b8dd1fc
caps.latest.revision: 6
ms.openlocfilehash: d2e5b8c0a7622481bfca21d5c5b46afa01c02d2c
ms.sourcegitcommit: b6871f21bd666f9cd71dd336bb3f844cf472b56c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/03/2019
ms.locfileid: "56863523"
---
# <a name="runspace03-c-code-sample"></a>RunSpace03 (C#) 代码示例

下面是C#中所述的控制台应用程序的源代码[创建指定脚本的控制台应用程序，运行](http://msdn.microsoft.com/en-us/a93e6006-36db-4bcc-b9da-c5bebf4ffd68)。 此示例使用[System.Management.Automation.Runspaceinvoke](/dotnet/api/System.Management.Automation.RunspaceInvoke)类，以执行检索使用传递到该脚本的进程名称的列表来处理信息的脚本。 它演示如何将输入的对象传递给脚本以及如何检索错误对象和输出对象。

> [!NOTE]
> 您可以下载C#使用 Microsoft Windows 软件开发工具包适用于 Windows Vista 和 Microsoft.NET Framework 3.0 运行时组件的此示例的源文件 (runspace03.cs)。 有关下载说明，请参阅[如何安装 Windows PowerShell 和下载 Windows PowerShell SDK](/powershell/developer/installing-the-windows-powershell-sdk)。
> 您可以下载C#使用 Microsoft Windows 软件开发工具包适用于 Windows Vista 和 Microsoft.NET Framework 3.0 运行时组件的此示例的源文件 (runspace03.cs)。 有关下载说明，请参阅[如何安装 Windows PowerShell 和下载 Windows PowerShell SDK](/powershell/developer/installing-the-windows-powershell-sdk)。
>
> 已下载的源文件中有 **\<PowerShell 示例 >** 目录。

## <a name="code-sample"></a>代码示例

[!code-csharp[Runspace03.cs](../../powershell-sdk-samples/SDK-2.0/csharp/Runspace03/Runspace03.cs#L11-L88 "Runspace03.cs")]

## <a name="see-also"></a>另请参阅

[Windows PowerShell 程序员指南](./windows-powershell-programmer-s-guide.md)

[Windows PowerShell SDK](../windows-powershell-reference.md)