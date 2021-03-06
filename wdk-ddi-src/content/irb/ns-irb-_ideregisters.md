---
UID: NS:irb._IDEREGISTERS
title: _IDEREGISTERS (irb.h)
description: The IDEREGISTERS structure is used to report the contents of the IDE controller registers.Note  The ATA port driver and ATA miniport driver models may be altered or unavailable in the future.
old-location: storage\ideregisters.htm
tech.root: storage
ms.date: 03/29/2018
keywords: ["IDEREGISTERS structure"]
ms.keywords: "*PIDEREGISTERS, IDEREGISTERS, IDEREGISTERS structure [Storage Devices], PIDEREGISTERS, PIDEREGISTERS structure pointer [Storage Devices], _IDEREGISTERS, irb/IDEREGISTERS, irb/PIDEREGISTERS, storage.ideregisters, structs-ATA_8e024553-553c-4a64-9f74-7259f530b3b5.xml"
req.header: irb.h
req.include-header: Irb.h
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
req.typenames: IDEREGISTERS, *PIDEREGISTERS
f1_keywords:
 - _IDEREGISTERS
 - irb/_IDEREGISTERS
 - PIDEREGISTERS
 - irb/PIDEREGISTERS
 - IDEREGISTERS
 - irb/IDEREGISTERS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - irb.h
api_name:
 - _IDEREGISTERS
 - PIDEREGISTERS
 - IDEREGISTERS
---

# _IDEREGISTERS structure


## -description

The IDEREGISTERS structure is used to report the contents of the IDE controller registers.
<div class="alert"><b>Note</b>  The ATA port driver and ATA miniport driver models may be altered or unavailable in the future. Instead, we recommend using the <a href="/windows-hardware/drivers/storage/storport-driver">Storport driver</a> and <a href="/windows-hardware/drivers/storage/storport-miniport-drivers">Storport miniport</a> driver models.</div><div> </div>

## -struct-fields

### -field bFeaturesReg

Specifies the contents of the ATA features register.

### -field bSectorCountReg

Specifies the contents of the ATA Sector Count register.

### -field bSectorNumberReg

Specifies the contents of the ATA Sector Number register.

### -field bCylLowReg

Specifies the contents of the ATA Cylinder Low register.

### -field bCylHighReg

Specifies the contents of the ATA Cylinder High register.

### -field bDriveHeadReg

Specifies the contents of the ATA Device/Head register.

### -field bCommandReg

Specifies the contents of the ATA Command register.

### -field bReserved

Reserved for future use. The miniport driver shall not use this field.

## -remarks

The information reported in the IDEREGISTERS structure is intended to be a superset of the information contained in <a href="/windows-hardware/drivers/ddi/ntdddisk/ns-ntdddisk-_ideregs">IDEREGS</a>. Microsoft might expand the contents of the IDEREGISTERS structure in the future. If you need a structure whose size is stable across different versions of the operating system, you should use <b>IDEREGS</b>.

## -see-also

<a href="/windows-hardware/drivers/ddi/ntdddisk/ns-ntdddisk-_ideregs">IDEREGS</a>

