---
title: IVMHardDiskConnectionCollection _NewEnum property (VPCCOMInterfaces.h)
description: Retrieves an enumerator for the collection.
ms.assetid: 9302f536-de25-4aac-88cf-9f4af6efcda7
keywords:
- _NewEnum property Virtual PC
- _NewEnum property Virtual PC , IVMHardDiskConnectionCollection interface
- IVMHardDiskConnectionCollection interface Virtual PC , _NewEnum property
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection._NewEnum
- IVMHardDiskConnectionCollection.get__NewEnum
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
---

# IVMHardDiskConnectionCollection::\_NewEnum property

\[Windows Virtual PC is no longer available for use as of Windows 8. Instead, use the [Hyper-V WMI provider (V2)](https://docs.microsoft.com/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Retrieves an enumerator for the collection.

This property is read-only.

## Syntax


```C++
HRESULT get__NewEnum(
  [out, retval] IUnknown **enumerator
);
```



## Property value

The [IEnumVARIANT](https://go.microsoft.com/fwlink/p/?linkid=120799) enumerator.

## Error codes



| Name/value                                                                                                                                                    | Meaning                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <dl> <dt>S\_OK</dt> <dt>0</dt> </dl>                       | The operation was successful.<br/> |
| <dl> <dt>E\_POINTER</dt> <dt>0x80004003</dt> </dl>         | The parameter is **NULL**.<br/>    |
| <dl> <dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt> </dl> | An unexpected error occurred.<br/> |



## Requirements



|                                     |                                                                                                    |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 7 \[desktop apps only\]<br/>                                                         |
| Minimum supported server<br/> | None supported<br/>                                                                          |
| End of client support<br/>    | Windows 7<br/>                                                                               |
| Product<br/>                  | Windows Virtual PC<br/>                                                                      |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl>      |
| IID<br/>                      | IID\_IVMHardDiskconnectionCollection is defined as b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## See also

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

 





