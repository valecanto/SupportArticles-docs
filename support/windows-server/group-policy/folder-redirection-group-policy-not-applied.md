---
title: Folder Redirection group policy is not applied
description: Addresses an issue that prevents folder redirection policy from working in SCCM on a computer that's running Windows 8, Windows 8.1, or Windows 10.
ms.date: 09/08/2020
author: Deland-Han
ms.author: delhan
manager: dscontentpm
audience: itpro
ms.topic: troubleshooting
ms.prod: windows-server
localization_priority: medium
ms.reviewer: kaushika
ms.prod-support-area-path: Problems applying Group Policy objects to users or computers
ms.technology: GroupPolicy
---
# Folder Redirection group policy is not applied in Windows 8, Windows 8.1, or Windows 10

This article helps fix an issue that prevents folder redirection policy from working in Microsoft System Center Configuration Manager (SCCM).

_Original product version:_ &nbsp; Windows 10, version 2004, Windows 10, version 1909, Windows 10, version 1809, Windows 10, version 1803, Windows 10, version 1709  
_Original KB number:_ &nbsp; 3060058

## Symptoms

Computers running Windows 8 and later versions may not apply Folder Redirection Group Policy objects (GPOs) as expected. This issue can occur if the computers are domain clients and are managed by System Center 2012 Configuration Manager Service Pack 1 (ConfigMgr 2012 SP1) or later. 

## Resolution

To work around this issue, disable the **Enable User Data and Profiles**  device setting in the System Center 2012 Configuration Manager console.

![Screenshot of the Enable User Data and Profiles option](./media/folder-redirection-group-policy-not-applied.md/enable-user-data-and-profiles-option.jpg)

For more information, see [How to create User Data and Profiles Configuration items in Configuration Manager](https://technet.microsoft.com/library/jj591610.aspx?f=255&mspperror=-2147217396).