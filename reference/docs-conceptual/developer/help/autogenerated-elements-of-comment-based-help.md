---
title: 基于注释的帮助的自动生成元素 |Microsoft Docs
ms.custom: ''
ms.date: 09/12/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 2a7098fe-0854-4fbb-83e9-073c20b299c7
caps.latest.revision: 4
ms.openlocfilehash: 0b8a32b5588e29148800daff8e104abba548eaf6
ms.sourcegitcommit: 52a67bcd9d7bf3e8600ea4302d1fa8970ff9c998
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "72367826"
---
# <a name="autogenerated-elements-of-comment-based-help"></a>基于注释的帮助的自动生成的元素

@No__t cmdlet 会自动生成基于注释的主题的几个元素。 这些自动生成的元素使基于注释的帮助看起来非常类似于从 XML 文件生成的帮助。

## <a name="autogenerated-elements"></a>自动生成元素

@No__t cmdlet 会自动生成帮助主题的以下元素。 你不能直接编辑这些元素，但在许多情况下，你可以通过更改元素的源来更改结果。

### <a name="name"></a>名称

函数帮助主题的 Name 节取自函数定义中的函数名。 脚本帮助主题的名称取自脚本文件名。 若要更改名称或其大小写，请更改函数定义或脚本文件名。

### <a name="syntax"></a>语法

帮助主题的语法部分是从函数或脚本的 Param 语句中的参数列表生成的。 若要将详细信息添加到帮助主题语法（如参数 .NET Framework 类型），请将详细信息添加到参数列表中。 如果未指定参数类型，则会将 "Object" 类型作为默认值插入。

### <a name="parameter-list"></a>参数列表

"帮助" 主题的 "参数" 部分是从函数或脚本中的参数列表生成的，也是通过使用参数列表中的 @no__t 0 关键字或注释添加的说明生成的。

参数在参数中的显示顺序与它们在参数列表中出现的顺序相同。 参数名称的拼写和大小写也是从参数列表中获取的;它不受 @no__t 关键字指定的参数名称的影响。

### <a name="common-parameters"></a>通用参数

公用参数将添加到帮助主题的语法和参数列表中，即使它们不起作用也是如此。 有关通用参数的详细信息，请参阅[about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)。

### <a name="parameter-attribute-table"></a>参数属性表

`Get-Help` 会生成参数表，当你使用 `Get-Help` 的 Full 或参数参数时，将显示这些属性。 "必需"、"位置" 和 "默认值" 属性的值取自函数或脚本语法。

### <a name="remarks"></a>备注

"帮助" 主题的 "备注" 部分是从函数或脚本名称自动生成的。 不能更改或影响其内容。
