---
Description: Flag that specifies whether the input stream is read-only. The upstream filter specifies this information when it calls the NotifyAllocator method. By default, the value is FALSE.
ms.assetid: d5a71c00-326c-45b4-b9c5-b67a0fe71bf5
title: CTransInPlaceInputPin::m\_bReadOnly member
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
topic_type: 
- APIRef
- kbSyntax
api_name: 
- m_bReadOnly
api_type: 
- LibDef
api_location: 
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
---

# CTransInPlaceInputPin::m\_bReadOnly member

Flag that specifies whether the input stream is read-only. The upstream filter specifies this information when it calls the [**NotifyAllocator**](ctransinplaceinputpin-notifyallocator.md) method. By default, the value is **FALSE**.

## Syntax


```C++
BOOL m_bReadOnly;
```



## Requirements



|                    |                                                                                                                                                                                            |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transip.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CTransInPlaceInputPin Class**](ctransinplaceinputpin.md)
</dt> </dl>

 

 



