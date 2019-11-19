---
keywords: powershell,cmdlet
ms.date: 11/19/2019
online version: https://docs.microsoft.com/zh-CN/powershell/module/microsoft.powershell.core/about/about_continue?view=powershell-6&WT.mc_id=ps-gethelp
schema: 2.0.0
title: about_Continue
---
# About Continue

## 简短描述

描述`Continue`语句如何立即返回程序流到程序循环的顶部

## 详细描述

在脚本中`Continue`语句立即返回程序流程到由`For`，`Foreach`或`While`语句控制的最内层循环的顶部。

`Continue`关键字支持标签。 标签是您分配给脚本中的语句。有关标签的信息，请参见 [about_Break](https://docs.microsoft.com/zh-CN/powershell/module/microsoft.powershell.core/about/about_Break?view=powershell-6&WT.mc_id=ps-gethelp)。

在下面的示例中，如果`$ctr`变量等于5，程序流返回到`While`循环的顶部。因此，显示5 除外1到10之间的其它数字：

```powershell
while ($ctr -lt 10)
{
    $ctr += 1
    if ($ctr -eq 5)
    {
        Continue
    }

    Write-Host -Object $ctr
}
```

当使用`For`循环时，执行将从`<重复>`语句继续，
 然后是`< 条件>`测试。 在下面的示例中，一个无限循环
 不会发生，因为`$i`的减量发生在`Continue`之后
 关键词。

```powershell
#   <初始值>  <条件> <重复>
for ($i = 0; $i -lt 10; $i++)
{
    Write-Host -Object $i
    if ($i -eq 5)
    {
        continue
        # 不会导致无限循环。
        $i--;
    }
}
```
