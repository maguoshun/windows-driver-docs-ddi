---
UID: NS:ndkpi._NDK_SGE
title: _NDK_SGE (ndkpi.h)
description: The NDK_SGE structure specifies the local buffers for NDK work requests.
old-location: netvista\ndk_sge.htm
tech.root: netvista
ms.date: 05/02/2018
keywords: ["NDK_SGE structure"]
ms.keywords: NDK_SGE, NDK_SGE structure [Network Drivers Starting with Windows Vista], _NDK_SGE, ndkpi/NDK_SGE, netvista.ndk_sge
req.header: ndkpi.h
req.include-header: Ndkpi.h
req.target-type: Windows
req.target-min-winverclnt: None supported,Supported in NDIS 6.30 and later.
req.target-min-winversvr: Windows Server 2012
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
req.typenames: NDK_SGE
f1_keywords:
 - _NDK_SGE
 - ndkpi/_NDK_SGE
 - NDK_SGE
 - ndkpi/NDK_SGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ndkpi.h
api_name:
 - _NDK_SGE
 - NDK_SGE
---

# _NDK_SGE structure


## -description

The  <b>NDK_SGE</b> structure specifies the local buffers for NDK work requests.

## -struct-fields

### -field VirtualAddress

A virtual address.

### -field LogicalAddress

A logical address.

### -field Length

The length, in bytes, of the buffer.

### -field MemoryRegionToken

A memory region token. When <b>MemoryRegionToken</b> is set to the token returned by <i>NdkGetPrivilegedMemoryRegionToken</i> (<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_get_privileged_memory_region_token">NDK_FN_GET_PRIVILEGED_MEMORY_REGION_TOKEN</a>), the <b>NDK_SGE</b> must contain a <b>LogicalAddress</b>. When <b>MemoryRegionToken</b> is not equal to the token returned by <i>NdkGetPrivilegedMemoryRegionToken</i>, the <b>NDK_SGE</b> structure must contain a <b>VirtualAddress</b>. When an <b>NDK_SGE</b> structure is used in a work request with the <b>NDK_OP_FLAG_INLINE</b> flag, <b>MemoryRegionToken</b> might be invalid. See the remarks section for more information about the <b>MemoryRegionToken</b>.

## -remarks

The <b>NDK_SGE</b> structure specifies the local buffers for send, receive, read, and write work requests. 

When the <b>MemoryRegionToken</b> member is set to the token returned by <i>NdkGetPrivilegedMemoryRegionToken</i> (<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_get_privileged_memory_region_token">NDK_FN_GET_PRIVILEGED_MEMORY_REGION_TOKEN</a>), the <b>NDK_SGE</b> must contain a logical address returned by the <i>NdkBuildLam</i> (<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_build_lam">NDK_FN_BUILD_LAM</a>) function with the <a href="/windows-hardware/drivers/ddi/ndkpi/ns-ndkpi-_ndk_logical_address_mapping">NDK_LOGICAL_ADDRESS_MAPPING</a> structure. Note that consecutive entries in the <b>AdapterPageArray</b> member of an <b>NDK_LOGICAL_ADDRESS_MAPPING</b> are not necessarily contiguous pages in the adapter's logical address space. Therefore, an NDK consumer might use multiple SGEs to cover all of the pages in an adapter page array.

When the token in the <b>MemoryRegionToken</b> member is not equal to the token that is returned by <i>NdkGetPrivilegedMemoryRegionToken</i>, the <b>NDK_SGE</b> structure must contain a virtual address that falls within the virtual address span of a previously registered memory region.

When an <b>NDK_SGE</b> structure is used in a work request with the <b>NDK_OP_FLAG_INLINE</b> flag,  the token in <b>MemoryRegionToken</b> might  be invalid, so it must be ignored by the NDK provider. When the <b>NDK_OP_FLAG_INLINE</b> flag is specified, the <b>VirtualAddress</b> member  of any <b>NDK_SGE</b> structure that is  passed to the work request function must point to a buffer that can be accessed by the NDK provider at an  IRQL less than or equal to  <b>DISPATCH_LEVEL</b>, That is, the buffer must be guaranteed to be resident in physical memory until the work request function returns. The total size of inline data that is passed to the provider in a single call must not exceed the  value in the  <i>InlineDataSize</i> parameter  that was  specified when the queue pair (QP) was  created.

## -see-also

<a href="/windows-hardware/drivers/network/ndkpi-object-lifetime-requirements">NDKPI Object Lifetime Requirements</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_build_lam">NDK_FN_BUILD_LAM</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_get_privileged_memory_region_token">NDK_FN_GET_PRIVILEGED_MEMORY_REGION_TOKEN</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_read">NDK_FN_READ</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_receive">NDK_FN_RECEIVE</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_send">NDK_FN_SEND</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_srq_receive">NDK_FN_SRQ_RECEIVE</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/nc-ndkpi-ndk_fn_write">NDK_FN_WRITE</a>



<a href="/windows-hardware/drivers/ddi/ndkpi/ns-ndkpi-_ndk_logical_address_mapping">NDK_LOGICAL_ADDRESS_MAPPING</a>

