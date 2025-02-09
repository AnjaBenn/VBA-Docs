---
title: Form.GoToPage method (Access)
keywords: vbaac10.chm13506
f1_keywords:
- vbaac10.chm13506
ms.prod: access
api_name:
- Access.Form.GoToPage
ms.assetid: 932c15b9-57dd-0cf7-1db2-21364bc214ea
ms.date: 03/09/2019
ms.localizationpriority: medium
---


# Form.GoToPage method (Access)

The **GoToPage** method moves the focus to the first control on a specified page in the active form.


## Syntax

_expression_.**GoToPage** (_PageNumber_, _Right_, _Down_)

_expression_ A variable that represents a **[Form](Access.Form.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _PageNumber_|Required|**Long**|A numeric expression that's a valid page number for the active form.|
| _Right_|Optional|**Long**|A numeric expression that's a valid horizontal offset (in [twips](../language/glossary/vbe-glossary.md#twip)) from the left side of the window to the part of the page to be viewed.|
| _Down_|Optional|**Long**|A numeric expression that's a valid vertical offset (in twips) from the top of the window to the part of the page to be viewed.|

## Remarks

When you use this method to move to a specified page of a form, the focus is set to the first control on the page, as defined by the form's tab order. To move to a particular control on the form, use the **SetFocus** method.

Use the **GoToPage** method if you've created page breaks on a form to group related information. For example, you might have an **Employees** form with personal information on the first page, office information on the second page, and sales information on the third page. Use the **GoToPage** method to move to the desired page.

Use the _Right_ and _Down_ arguments for forms with pages larger than the Microsoft Access window. Use the _PageNumber_ argument to move to the desired page, and then use the _Right_ and _Down_ arguments to display the part of the page that you want to see. Access displays the part of the page that's offset from the upper-left corner of the window by the distance specified in the _Right_ and _Down_ arguments.


## Example

The following example uses the **GoToPage** method to move the focus to the second page of the **Customer** form at the position specified by the _Right_ and _Down_ arguments.

```vb
Forms!Customer.GoToPage 2, 1440, 600
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]