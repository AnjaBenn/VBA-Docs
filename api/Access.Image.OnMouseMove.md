---
title: Image.OnMouseMove property (Access)
keywords: vbaac10.chm10397
f1_keywords:
- vbaac10.chm10397
ms.prod: access
api_name:
- Access.Image.OnMouseMove
ms.assetid: 9890dd97-0025-7329-1751-82d69799510d
ms.date: 02/23/2019
ms.localizationpriority: medium
---


# Image.OnMouseMove property (Access)

Sets or returns the value of the **On Mouse Move** box in the Properties window. Read/write **String**.


## Syntax

_expression_.**OnMouseMove**

_expression_ A variable that represents an **[Image](Access.Image.md)** object.


## Remarks

This property is helpful for programmatically changing the action that Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The **MouseMove** event occurs when the user moves the mouse over the object.

The **OnMouseMove** value will be one of the following, depending on the selection chosen in the Choose Builder window (accessed by choosing the **Build** button next to the **On Mouse Move** box in the object's Properties window):

- If you choose Expression Builder, the value will be =_expression_, where _expression_ is the expression from the Expression Builder window.
    
- If you choose Macro Builder, the value is the name of the macro. 
    
- If you choose Code Builder, the value will be [Event Procedure]. 
    
If the **On Mouse Move** box is blank, the property value is an empty string.


## Example

The following example prints the value of the **OnMouseMove** property in the Immediate window for the button named **OK** on the **Order Entry** form.

```vb
Debug.Print Forms("Order Entry").Controls("OK").OnMouseMove
```


[!include[Support and feedback](~/includes/feedback-boilerplate.md)]