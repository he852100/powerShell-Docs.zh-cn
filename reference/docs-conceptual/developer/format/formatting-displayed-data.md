---
title: 设置显示的数据的格式 |Microsoft Docs
ms.custom: ''
ms.date: 09/12/2016
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 38971643-2a3d-4f5b-a1fa-6334c162b8ed
caps.latest.revision: 4
ms.openlocfilehash: e915ac71feb50cb58cfa9195f0de94763affdb77
ms.sourcegitcommit: 52a67bcd9d7bf3e8600ea4302d1fa8970ff9c998
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/15/2019
ms.locfileid: "72363696"
---
# <a name="formatting-displayed-data"></a>设置显示数据的格式

您可以指定如何显示列表、表或宽视图中的各个数据点。 在定义视图的项时，可以使用 `FormatString` 元素，也可以使用 @no__t 元素对数据调用 `FormatString` 方法。

## <a name="using-the-formatstring-element"></a>使用格式字符串元素

在下面的示例中，使用 "格式字符串" 元素设置 "@no__t [" 对象的值。](/dotnet/api/System.Diagnostics.Process) `TotalProcessorTime` 属性

```
<TableColumnItem>
  <PropertyName>TotalProcessorTime</PropertyName>
  <FormatString>{0:MMM}{0:dd}{0:HH}:{0:mm}</FormatString>
</TableColumnItem>
```



