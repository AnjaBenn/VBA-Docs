---
title: Report.KeyDown event (Access)
keywords: vbaac10.chm13894
f1_keywords:
- vbaac10.chm13894
ms.prod: access
api_name:
- Access.Report.KeyDown
ms.assetid: b33ecbca-b3a1-19b2-8541-fe4bcbf4acec
ms.date: 02/10/2019
ms.localizationpriority: medium
---


# Report.KeyDown event (Access)

The **KeyDown** event occurs when the user presses a key while a report has the focus. This event also occurs if you send a keystroke to a report by using the SendKeys action in a macro or the **SendKeys** statement in Visual Basic.


## Syntax

_expression_.**KeyDown** (_KeyCode_, _Shift_)

_expression_ A variable that represents a **[Report](Access.Report.md)** object.


## Parameters

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
| _KeyCode_|Required|**Integer**|A key code, such as **vbKeyF1** (the F1 key) or **vbKeyHome** (the Home key). To specify key codes, use the intrinsic constants shown in the Object Browser. You can prevent an object from receiving a keystroke by setting _KeyCode_ to 0.|
| _Shift_|Required|**Integer**|The state of the Shift, Ctrl, and Alt keys at the time of the event. If you need to test for the _Shift_ argument, you can use one of the following intrinsic constants as bit masks:<ul><li><p><b>acShiftMask</b>  The bit mask for the Shift key.</p></li><li><p><b>acCtrlMask</b>  The bit mask for the Ctrl key.</p></li><li><p><b>acAltMask</b>  The bit mask for the Alt key.</p></li></ul> |

## Remarks

The **KeyDown** event applies only to forms and controls on a form, and not to controls on a report.

To run a macro or event procedure when these events occur, set the **OnKeyDown** property to the name of the macro or to [Event Procedure].

A report will also receive all keyboard events, even those that occur for controls, if you set the **KeyPreview** property of the report to Yes. With this property setting, all keyboard events occur first for the report, and then for the control that has the focus. You can respond to specific keys pressed in the report, regardless of which control has the focus. For example, you may want the key combination Ctrl+X to always perform the same action on a report.

If you press and hold down a key, the **KeyDown** and **KeyPress** events alternate repeatedly (**KeyDown**, **KeyPress**, **KeyDown**, **KeyPress**, and so on) until you release the key, and then the **KeyUp** event occurs.

Although the **KeyDown** event occurs when most keys are pressed, it is typically used to recognize or distinguish between:

- Extended character keys, such as function keys.
    
- Navigation keys, such as Home, End, PgUp, PgDn, Up arrow, Down arrow, Right arrow, Left arrow, and Tab.
    
- Combinations of keys and standard keyboard modifiers (Shift, Ctrl, or Alt keys).
    
- The numeric keypad and keyboard number keys.
    
To find out the ANSI character corresponding to the key pressed, use the **KeyPress** event.

If a modal dialog box is displayed as a result of pressing or sending a key, the **KeyDown** and **KeyPress** events occur, but the **KeyUp** event doesn't occur.




[!include[Support and feedback](~/includes/feedback-boilerplate.md)]