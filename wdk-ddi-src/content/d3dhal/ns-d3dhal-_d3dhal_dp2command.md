---
UID: NS:d3dhal._D3DHAL_DP2COMMAND
title: _D3DHAL_DP2COMMAND (d3dhal.h)
description: One or more D3DHAL_DP2COMMAND structures are parsed from the command buffer by the D3dDrawPrimitives2 callback, which uses the information it receives to draw one or more primitives.
old-location: display\d3dhal_dp2command.htm
tech.root: display
ms.date: 05/10/2018
keywords: ["D3DHAL_DP2COMMAND structure"]
ms.keywords: "*LPD3DHAL_DP2COMMAND, D3DHAL_DP2COMMAND, D3DHAL_DP2COMMAND structure [Display Devices], LPD3DHAL_DP2COMMAND, LPD3DHAL_DP2COMMAND structure pointer [Display Devices], _D3DHAL_DP2COMMAND, d3dhal/D3DHAL_DP2COMMAND, d3dhal/LPD3DHAL_DP2COMMAND, d3dstrct_9497e802-c325-4d08-ba6c-f482d17da6c5.xml, display.d3dhal_dp2command"
req.header: d3dhal.h
req.include-header: D3dhal.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: D3DHAL_DP2COMMAND, *LPD3DHAL_DP2COMMAND
f1_keywords:
 - _D3DHAL_DP2COMMAND
 - d3dhal/_D3DHAL_DP2COMMAND
 - LPD3DHAL_DP2COMMAND
 - d3dhal/LPD3DHAL_DP2COMMAND
 - D3DHAL_DP2COMMAND
 - d3dhal/D3DHAL_DP2COMMAND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dhal.h
api_name:
 - _D3DHAL_DP2COMMAND
 - LPD3DHAL_DP2COMMAND
 - D3DHAL_DP2COMMAND
---

# _D3DHAL_DP2COMMAND structure


## -description

One or more D3DHAL_DP2COMMAND structures are parsed from the command buffer by the <a href="/windows-hardware/drivers/ddi/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> callback, which uses the information it receives to draw one or more primitives. Each structure specifies either a primitive to draw or a state change to process.

## -struct-fields

### -field bCommand

Specifies a primitive to draw or a state change to process. This member can be one of the <a href="/windows-hardware/drivers/ddi/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DHAL_DP2OPERATION</a> enumerated values.

### -field bReserved

Reserved for system use and should be ignored by the driver.

### -field wPrimitiveCount

Specifies the number of primitives to process. This member is valid when <b>bCommand</b> is not either of D3DDP2OP_RENDERSTATE or D3DDP2OP_TEXTURESTAGESTATE.

### -field wStateCount

Specifies the number of state changes to process. This member is valid when <b>bCommand</b> is one of D3DDP2OP_RENDERSTATE or D3DDP2OP_TEXTURESTAGESTATE.

## -see-also

D3DDP2OP_RENDERSTATE



D3DDP2OP_TEXTURESTAGESTATE



<a href="/windows-hardware/drivers/ddi/d3dhal/ne-d3dhal-_d3dhal_dp2operation">D3DHAL_DP2OPERATION</a>



<a href="/windows-hardware/drivers/ddi/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a>

