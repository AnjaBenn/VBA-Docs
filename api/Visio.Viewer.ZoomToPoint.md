---
title: Viewer.ZoomToPoint method (Visio Viewer)
ms.prod: visio
api_name:
- Visio.Viewer.ZoomToPoint
ms.assetid: 3eb5c8f9-ced0-a35b-172a-337f25a68d98
ms.date: 06/21/2019
ms.localizationpriority: medium
---


# Viewer.ZoomToPoint method (Visio Viewer)

Resizes the drawing that is open in Microsoft Visio Viewer to the specified percentage of its previous size, and places the upper-left corner of the drawing at the specified point in the Visio Viewer window, measured in pixels in the coordinate system of the window. 


## Syntax

_expression_.**ZoomToPoint** (_X_, _Y_, _Percentage_)

_expression_ An expression that returns a **[Viewer](Visio.Viewer.md)** object.


## Parameters 

|Name|Required/Optional|Data type|Description|
|:-----|:-----|:-----|:-----|
|_X_|Required| **Long**|The x-coordinate, in pixels in the coordinate system of the Visio Viewer window, of the point to place the upper-left corner of the drawing.|
|_Y_|Required| **Long**|The y-coordinate, in pixels in the coordinate system of the Visio Viewer window, of the point to place the upper-left corner of the drawing.|
|_Percentage_|Required| **Double**|The percentage of zoom.|

## Return value

Nothing


## Remarks

Setting the _Percentage_ parameter to 1 displays the drawing at its original size. Setting it to 2 doubles the length on both sides of the drawing by that factor, thus quadrupling the size of the drawing. Setting it to 0.5 displays the page at one-quarter its original size.

The origin of the coordinate system of the Visio Viewer window is its upper-left corner. The positive x-direction is to the right, and the positive y-direction is down.


## Example

The following code displays the drawing at half its previous size, and places the upper-left corner of the drawing at a point 200 pixels to the right and 200 pixels below the upper-left corner of the Visio Viewer window.

```vb
vsoViewer.ZoomToPoint 200, 200, 0.5
```

[!include[Support and feedback](~/includes/feedback-boilerplate.md)]