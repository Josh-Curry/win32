---
title: DPI compensation effect
description: Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context. This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# DPI compensation effect

Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context. This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.

The CLSID for this effect is CLSID\_D2D1DpiCompensation.

## Effect properties



| Display name and index enumeration                                                       | Description                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InterpolationMode<br/> D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE<br/> | The interpolation mode the effect uses to scale the image.<br/> The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.<br/> The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .<br/>                  |
| BorderMode<br/> D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE<br/>               | The mode used to calculate the border of the image, soft or hard. See [Border modes](https://www.bing.com/search?q=Border modes) for more info. <br/> The type is D2D1\_BORDER\_MODE.<br/> The default value is D2D1\_BORDER\_MODE\_SOFT.<br/> |
| InputDpi<br/> D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI<br/>                   | The DPI of the input image.<br/> The type is FLOAT.<br/> The default value is 96.0f.<br/>                                                                                                                                    |



 

## Interpolation modes



| Enumeration                                                       | Description                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR     | Samples the nearest single point and uses that. This mode uses less processing time, but outputs the lowest quality image.                                                                           |
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR                | Uses a four point sample and linear interpolation. This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.                                           |
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC                 | Uses a 16 sample cubic kernel for interpolation. This mode uses the most processing time, but outputs a higher quality image.                                                                        |
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR | Uses 4 linear samples within a single pixel for good edge anti-aliasing. This mode is good for scaling down by small amounts on images with few pixels.                                              |
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC           | Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.                                                                                                     |
| D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC  | Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix. Then uses the cubic interpolation mode for the final output. |



 

> [!Note]  
> If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.

 

## Border modes



| Name                     | Description                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| D2D1\_BORDER\_MODE\_SOFT | Pixels outside of the input boundaries are generated by the [mirror border effect](border.md). <br/> |
| D2D1\_BORDER\_MODE\_HARD | Pixels outside of the input boundaries are transparent black.<br/>                                    |



 

## Requirements



|                          |                                                                                    |
|--------------------------|------------------------------------------------------------------------------------|
| Minimum supported client | Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\] |
| Minimum supported server | Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\] |
| Header                   | d2d1effects.h                                                                      |
| Library                  | d2d1.lib, dxguid.lib                                                               |



 

## Related topics

<dl> <dt>

[**ID2D1Effect**](/windows/desktop/api/D2d1_1/)
</dt> </dl>

 

 




