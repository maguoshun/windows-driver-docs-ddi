---
UID: NS:hbapiwmi._GetEventBuffer_OUT
title: _GetEventBuffer_OUT (hbapiwmi.h)
description: The GetEventBuffer_OUT structure is used to report the output parameter data of the GetEventBuffer WMI method to the WMI client.
old-location: storage\geteventbuffer_out.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["GetEventBuffer_OUT structure"]
ms.keywords: "*PGetEventBuffer_OUT, GetEventBuffer_OUT, GetEventBuffer_OUT structure [Storage Devices], PGetEventBuffer_OUT, PGetEventBuffer_OUT structure pointer [Storage Devices], _GetEventBuffer_OUT, hbapiwmi/GetEventBuffer_OUT, hbapiwmi/PGetEventBuffer_OUT, storage.geteventbuffer_out, structs-Fibre_af1916c9-60f8-4601-b9dd-d4575a100d98.xml"
req.header: hbapiwmi.h
req.include-header: Hbapiwmi.h
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
req.typenames: GetEventBuffer_OUT, *PGetEventBuffer_OUT
f1_keywords:
 - _GetEventBuffer_OUT
 - hbapiwmi/_GetEventBuffer_OUT
 - PGetEventBuffer_OUT
 - hbapiwmi/PGetEventBuffer_OUT
 - GetEventBuffer_OUT
 - hbapiwmi/GetEventBuffer_OUT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - hbapiwmi.h
api_name:
 - _GetEventBuffer_OUT
 - PGetEventBuffer_OUT
 - GetEventBuffer_OUT
---

# _GetEventBuffer_OUT structure


## -description

The GetEventBuffer_OUT structure is used to report the output parameter data of the <a href="/windows-hardware/drivers/storage/geteventbuffer">GetEventBuffer</a> WMI method to the WMI client.

## -struct-fields

### -field HBAStatus

Contains a value associated with the WMI class qualifier <a href="/windows-hardware/drivers/storage/hba-status">HBA_STATUS</a> that indicates the result of an HBA query operation.

### -field EventCount

Indicates the number of events in <b>Events</b> that were retrieved by the <a href="/windows-hardware/drivers/storage/geteventbuffer">GetEventBuffer</a> WMI method.

### -field Events

Contains an array of type <a href="/windows-hardware/drivers/ddi/hbapiwmi/ns-hbapiwmi-_msfc_eventbuffer">MSFC_EventBuffer</a> that contains the next events in the HBA's event queue.

## -remarks

The <a href="/windows-hardware/drivers/storage/geteventbuffer">GetEventBuffer</a> method retrieves the next events in the HBA's event queue. 

The WMI tool suite generates a declaration of the GetEventBuffer_OUT structure in <i>Hbapiwmi.h </i>when it compiles the <a href="/windows-hardware/drivers/storage/msfc-hbaadaptermethods-wmi-class">MSFC_HBAAdapterMethods WMI Class</a>.

## -see-also

<a href="/windows-hardware/drivers/storage/geteventbuffer">GetEventBuffer</a>

