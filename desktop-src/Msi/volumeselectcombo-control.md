---
Description: The VolumeSelectCombo control enables the user to select a volume from an alphabetical list of volumes.
ms.assetid: 5d486ca8-4c8a-4a15-9d38-7430d0a169ed
title: VolumeSelectCombo Control
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# VolumeSelectCombo Control

The VolumeSelectCombo control enables the user to select a volume from an alphabetical list of volumes. The types of volumes displayed in the list are specified using bits associated with [RemovableVolume](removablevolume-control-attribute.md), [FixedVolume](fixedvolume-control-attribute.md), [RemoteVolume](remotevolume-control-attribute.md), [CDROMVolume](cdromvolume-control-attribute.md), [RAMDiskVolume](ramdiskvolume-control-attribute.md), and [FloppyVolume](floppyvolume-control-attribute.md) control attributes.

You can associate this control with a property by entering the property's name in the Property column of the [Control table](control-table.md).

## Control Attributes

You can use the following attributes with this control. To change the value of an attribute using an event, subscribe the control to a ControlEvent in the [EventMapping table](eventmapping-table.md) and list the attribute's identifier in the Attribute column. Enter the identifier of the ControlEvent in the Event column.



| Attribute identifier                                               | Hexadecimal bit                  | Description                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IndirectPropertyName](indirectpropertyname-control-attribute.md) |                                  | This is the name of an indirect property associated with the control. If the Indirect attribute bit is set, the control displays or changes the value of the property having this name. If the Indirect attribute bit is set, this name is also the value of the property listed in the Property column of the [Control table](control-table.md).                                   |
| [Position](position-control-attribute.md)                         |                                  | Position of control in the dialog box. Enter the control's width, height, and coordinates of the control's left corner into the Width, Height, X, and Y columns of the [Control table](control-table.md). Use [installer units](installer-units.md) for length and distance.<br/>                                                                                            |
| [PropertyName](propertyname-control-attribute.md)                 |                                  | This is the name of the property associated with this control. If the Indirect attribute bit is not set, the control displays or changes the value of the property having this name. This attribute is specified in the Property column of the [Control table](control-table.md).                                                                                                   |
| [PropertyValue](propertyvalue-control-attribute.md)               |                                  | Current value of the property displayed or changed by this control. If the Indirect attribute bit is not set, this is the value of PropertyName. If the Indirect attribute bit is set, this is the value of IndirectPropertyName. If the attribute changes, the control reflects the new value.                                                                                      |
| [Text](text-control-attribute.md)                                 |                                  | To set the font and font style of a text string, prefix the string of displayed characters with {\\style} or {&style}. Where style is an identifier listed in the TextStyle column of the [TextStyle table](textstyle-table.md). If neither of these are present, but the [**DefaultUIFont**](defaultuifont.md) property is defined as a valid text style, that font will be used. |
| [Visible](visible-control-attribute.md)                           | 0x00000000 0x00000001<br/> | Hidden control. Visible control.<br/> Include this bit in the bit word of the Attributes column in the [Control table](control-table.md) to make the control visible or hidden upon its creation.<br/> You can also hide or show a control by using the [ControlCondition table](controlcondition-table.md).<br/>                                                |
| [Enabled](enabled-control-attribute.md)                           | 0x00000000 0x00000002<br/> | Control in a disabled state. Control in an enabled state.<br/> Include this bit in the bit word in the Attributes column of the [Control](control-table.md) to enable the control on creation.<br/> You can also enable or disable a control by using the [ControlCondition table](controlcondition-table.md).<br/>                                              |
| [Sunken](sunken-control-attribute.md)                             | 0x00000000 0x00000004<br/> | Displays the default visual style. Displays the control with a sunken, 3-D, look.<br/> Include these bits in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                       |
| [Indirect](indirect-control-attribute.md)                         | 0x00000000 0x00000008<br/> | The control displays or changes the value of the property in the Property column of the [Control table](control-table.md). The control displays or changes the value of the property that has the Identifier listed in the Property column of the Control table.<br/> Determines if the property associated with this control is referenced indirectly.<br/>            |
| [RTLRO](rtlro-control-attribute.md)                               | 0x00000000 0x00000020<br/> | Text in the control is displayed in left-to-right reading order. Text in the control is displayed in right-to-left reading order.<br/>                                                                                                                                                                                                                                         |
| [RightAligned](rightaligned-control-attribute.md)                 | 0x00000000 0x00000040<br/> | Text in the control is aligned to the left. Text in the control is aligned to the right.<br/>                                                                                                                                                                                                                                                                                  |
| [LeftScroll](leftscroll-control-attribute.md)                     | 0x00000000 0x00000080<br/> | The scroll bar is located on the right side of the control. The scroll bar is located on the left side of the control.<br/>                                                                                                                                                                                                                                                    |
| [BiDi](bidi-control-attribute.md)                                 | 0x000000E0                       | Set this value for a combination of the [RTLRO](rtlro-control-attribute.md), [RightAligned](rightaligned-control-attribute.md), and [LeftScroll](leftscroll-control-attribute.md) attributes.                                                                                                                                                                                     |
| [RemovableVolume](removablevolume-control-attribute.md)           | 0x00010000                       | Control lists removable drives. Include in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                               |
| [FixedVolume](fixedvolume-control-attribute.md)                   | 0x00020000                       | Control lists fixed internal hard drives. Include in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                     |
| [RemoteVolume](remotevolume-control-attribute.md)                 | 0x00040000                       | Control lists remote volumes. Include in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                                 |
| [CDROMVolume](cdromvolume-control-attribute.md)                   | 0x00080000                       | Control lists CD-ROM volumes. Include in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                                 |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)               | 0x00100000                       | Control lists RAM disks. Include in the bit word in the Attributes column of the [Control table](control-table.md)..<br/>                                                                                                                                                                                                                                                     |
| [FloppyVolume](floppyvolume-control-attribute.md)                 | 0x00200000                       | Control lists floppy drives. Include in the bit word in the Attributes column of the [Control table](control-table.md).<br/>                                                                                                                                                                                                                                                  |



 

## Remarks

This control can be created from the COMBOBOX class by using the [**CreateWindowEx**](https://msdn.microsoft.com/library/ms632680(v=VS.85).aspx) function. It has the **CBS\_DROPDOWNLIST**, **CBS\_OWNERDRAWFIXED**, **CBS\_HASSTRINGS**, **WS\_VSCROLL**, **WS\_CHILD**, **WS\_GROUP**, **WS\_TABSTOP**, and **CBS\_SORT** styles. For information about developing a user interface with Windows, see [User Interface Design and Development](Http://go.microsoft.com/fwlink/p/?linkid=83878).

For compatibility with screen readers, when authoring a dialog box with a VolumeSelectCombo control as the first active control, you must make the text field belonging to the edit field the first active control in the [Dialog table](dialog-table.md). Since the static text cannot take focus, when the dialog box is created, the edit field will have the focus initially as intended. This ensures that screen readers show the correct information.

 

 



