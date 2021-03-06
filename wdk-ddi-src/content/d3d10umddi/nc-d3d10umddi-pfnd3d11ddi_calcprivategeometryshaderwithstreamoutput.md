---
UID: NC:d3d10umddi.PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT
title: PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT (d3d10umddi.h)
description: The CalcPrivateGeometryShaderWithStreamOutput(D3D11) function determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a geometry shader with stream output.
old-location: display\calcprivategeometryshaderwithstreamoutput_d3d11_.htm
ms.date: 05/10/2018
keywords: ["PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT callback function"]
ms.keywords: CalcPrivateGeometryShaderWithStreamOutput, CalcPrivateGeometryShaderWithStreamOutput callback function [Display Devices], PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT, PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT callback, UserModeDisplayDriverDx11_Functions_7345bace-3d45-45fe-a0f5-ee76a842c998.xml, d3d10umddi/CalcPrivateGeometryShaderWithStreamOutput, display.calcprivategeometryshaderwithstreamoutput_d3d11_
req.header: d3d10umddi.h
req.include-header: D3d10umddi.h
req.target-type: Desktop
req.target-min-winverclnt: CalcPrivateGeometryShaderWithStreamOutput(D3D11) is supported beginning with the Windows 7 operating system.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
tech.root: display
req.typenames: 
f1_keywords:
 - PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT
 - d3d10umddi/PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - d3d10umddi.h
api_name:
 - PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT
---

# PFND3D11DDI_CALCPRIVATEGEOMETRYSHADERWITHSTREAMOUTPUT callback function


## -description

The <i>CalcPrivateGeometryShaderWithStreamOutput(D3D11)</i> function determines the size of the user-mode display driver's private region of memory (that is, the size of internal driver structures, not the size of the resource video memory) for a geometry shader with stream output.

## -parameters

### -param Arg1

*hDevice* [in]

A handle to the display device (graphics context).

### -param Arg2

*pCreateGeometryShaderWithStreamOutput* [in]


A pointer to a <a href="/windows-hardware/drivers/ddi/d3d10umddi/ns-d3d10umddi-d3d11ddiarg_creategeometryshaderwithstreamoutput">D3D11DDIARG_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT</a> structure that describes the parameters that the user-mode display driver uses to calculate the size of the memory region.

### -param Arg3

*pSignatures* [in]

A pointer to a <a href="/windows-hardware/drivers/ddi/d3d10umddi/ns-d3d10umddi-d3d10ddiarg_stage_io_signatures">D3D10DDIARG_STAGE_IO_SIGNATURES</a> structure that forms the shader's signature.

## -returns

<i>CalcPrivateGeometryShaderWithStreamOutput(D3D11)</i> returns the size of the memory region that the driver requires to create a geometry shader with stream output.

## -see-also

<a href="/windows-hardware/drivers/ddi/d3d10umddi/ns-d3d10umddi-d3d10ddiarg_stage_io_signatures">D3D10DDIARG_STAGE_IO_SIGNATURES</a>



<a href="/windows-hardware/drivers/ddi/d3d10umddi/ns-d3d10umddi-d3d11ddiarg_creategeometryshaderwithstreamoutput">D3D11DDIARG_CREATEGEOMETRYSHADERWITHSTREAMOUTPUT</a>



<a href="/windows-hardware/drivers/ddi/d3d10umddi/ns-d3d10umddi-d3d11ddi_devicefuncs">D3D11DDI_DEVICEFUNCS</a>

