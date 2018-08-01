---
Description: The Win32\_SystemConfigurationChangeEvent&\#8194;WMI class indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed).
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: dce1e866-e739-4f90-9016-48b20ccfb75b
ms.prod: windows-server-dev
ms.technology:
- cimwin32
- windows-management-instrumentation
ms.tgt_platform: multiple
title: Win32\_SystemConfigurationChangeEvent class
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemConfigurationChangeEvent
- Win32_SystemConfigurationChangeEvent.SECURITY_DESCRIPTOR
- Win32_SystemConfigurationChangeEvent.TIME_CREATED
- Win32_SystemConfigurationChangeEvent.EventType
api_type:
- DllExport
api_location:
- CIMWin32.dll
---

# Win32\_SystemConfigurationChangeEvent class

The **Win32\_SystemConfigurationChangeEvent** [WMI class](https://msdn.microsoft.com/en-us/library/Aa393244(v=VS.85).aspx) indicates that the device list on the system has been refreshed (a device has been added or removed, or the configuration changed). An event is fired and an instance of this is class created when the "DevMgrRefreshOn&lt;*ComputerName*&gt;" message is sent. The exact change to the device list is not contained in the message, so a device refresh is required to obtain the current system settings. Examples of configuration changes affected are IRQ settings, COM ports, and BIOS versions.

The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties. Properties and methods are in alphabetic order, not MOF order.

## Syntax

``` syntax
[UUID("76746942-D94B-47E2-BBA4-AFD2FDBA61"), AMENDMENT]
class Win32_SystemConfigurationChangeEvent : Win32_DeviceChangeEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint16 EventType;
};
```

## Members

The **Win32\_SystemConfigurationChangeEvent** class has these types of members:

-   [Properties](#properties)

### Properties

The **Win32\_SystemConfigurationChangeEvent** class has these properties.

<dl> <dt>

**EventType**
</dt> <dd> <dl> <dt>

Data type: **uint16**
</dt> <dt>

Access type: Read-only
</dt> <dt>

Qualifiers: [**MappingStrings**](https://msdn.microsoft.com/en-us/library/Aa393650(v=VS.85).aspx) ("Win32APIDevice Management Messages\|WM\_DEVICECHANGE\|wParam", "Win32APIDevice Management Messages\|WM\_SETTINGCHANGE")
</dt> </dl>

Type of event change notification that has occurred.

This property is inherited from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).

<dt>

<span id="Configuration_Changed"></span><span id="configuration_changed"></span><span id="CONFIGURATION_CHANGED"></span>

**Configuration Changed** (1)


</dt> <dd></dd> <dt>

<span id="Device_Arrival"></span><span id="device_arrival"></span><span id="DEVICE_ARRIVAL"></span>

**Device Arrival** (2)


</dt> <dd></dd> <dt>

<span id="Device_Removal"></span><span id="device_removal"></span><span id="DEVICE_REMOVAL"></span>

**Device Removal** (3)


</dt> <dd></dd> <dt>

<span id="Docking"></span><span id="docking"></span><span id="DOCKING"></span>

**Docking** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**SECURITY\_DESCRIPTOR**
</dt> <dd> <dl> <dt>

Data type: **uint8** array
</dt> <dt>

Access type: Read-only
</dt> </dl>

Descriptor used by the event provider to determine which users can receive the event. This property is inherited from [**\_\_Event**](https://msdn.microsoft.com/en-us/library/Aa394634(v=VS.85).aspx). For more information about constants used to set this security descriptor, see [WMI Security Constants](https://msdn.microsoft.com/en-us/library/Aa394576(v=VS.85).aspx).

</dd> <dt>

**TIME\_CREATED**
</dt> <dd> <dl> <dt>

Data type: **uint64**
</dt> <dt>

Access type: Read-only
</dt> </dl>

Unique value that indicates the time at which the event was generated. This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601. The information is in the Coordinated Universal Times (UTC) format.

This property is inherited from [**\_\_Event**](https://msdn.microsoft.com/en-us/library/Aa394634(v=VS.85).aspx).

For more information about using **uint64** values in scripts, see [Scripting in WMI](https://msdn.microsoft.com/library/Aa389763(v=VS.85).aspx).

</dd> </dl>

## Remarks

The **Win32\_SystemConfigurationChangeEvent** class is derived from [**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md).

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                                |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root\\CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## See also

<dl> <dt>

[**Win32\_DeviceChangeEvent**](win32-devicechangeevent.md)
</dt> <dt>

[Operating System Classes](https://msdn.microsoft.com/en-us/library/Dn792258(v=VS.85).aspx)
</dt> </dl>

 

 



