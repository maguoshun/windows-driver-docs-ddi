---
UID: NF:dbgmodel.IDebugHostField.GetLocation
title: IDebugHostField::GetLocation (dbgmodel.h)
description: For fields which have an address regardless of the particular type instance (e.g. fields whose location kind indicates LocationStatic), the GetLocation method will return the abstract location (address) of the field.
ms.date: 09/12/2018
keywords: ["IDebugHostField::GetLocation"]
ms.keywords: IDebugHostField::GetLocation, GetLocation, IDebugHostField.GetLocation, IDebugHostField::GetLocation, IDebugHostField.GetLocation
req.header: dbgmodel.h
req.include-header: 
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.lib: 
req.dll: 
req.irql: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
targetos: Windows
tech.root: debugger
ms.custom: RS5
f1_keywords:
 - IDebugHostField::GetLocation
 - dbgmodel/IDebugHostField::GetLocation
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - dbgmodel.h
api_name:
 - IDebugHostField::GetLocation
---

# IDebugHostField::GetLocation


## -description

For fields which have an address regardless of the particular type instance (e.g. fields whose location kind indicates LocationStatic), the GetLocation method will return the abstract location (address) of the field.

If the given field does not have a static location, the GetLocation method will fail.

## -parameters

### -param location

The abstract location (e.g.: address) of the field will be returned here.

## -returns

This method returns HRESULT which indicates success or failure.

## -remarks

**Sample Code***
```cpp
ComPtr<IDebugHostField> spField; /* get a field symbol (see EnumerateChildren) */

Location fieldLocation;
if (SUCCEEDED(spField->GetLocation(&fieldLocation)))
{
    // For fields which have a static location as determined by GetLocationKind, 
    // the location of the field will be in fieldLocation.
}
```

## -see-also

[IDebugHostField interface](nn-dbgmodel-idebughostfield.md)

