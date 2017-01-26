---
author: brianlic-msft
description: 
external help file: StorageScripts-help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Disable-StorageMaintenanceMode
ms.assetid: F65A87E5-14E3-4323-B261-98AA687F6EF1
---

# Disable-StorageMaintenanceMode

## SYNOPSIS
Disables storage maintenance mode on a fault domain.

## SYNTAX

```
Disable-StorageMaintenanceMode -InputObject <CimInstance> [-Model <String>] [-Manufacturer <String>]
 [-CimSession <CimSession>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-StorageMaintenanceMode** cmdlet disables storage maintenance mode on a fault domain, which includes SSU, StorageEnclosure, and PhysicalDisk.

## EXAMPLES

### Example 1: Disable maintenance mode on a physical disk
```
PS C:\>Get-PhysicalDisk -FriendlyName "Disk22" | Disable-StorageMaintenanceMode
```

This command gets a physical disk by using the Get-PhysicalDisk cmdlet, and then passes that object to the current cmdlet.
The command disables storage maintenance mode on the disk named Disk22.

## PARAMETERS

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: CimInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Manufacturer
Specifies the manufacturer of a device.
This cmdlet matches manufacturer information of physical disk devices, and disables maintenance mode on those devices.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Model
Specifies the model of a physical disk device that this cmdlet removes from maintenance mode.
If multiple devices fit a model string, this cmdlet removes those devices from maintenance mode.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### MSFT_StorageFaultDomain
You can pipe a fault domain object, **PhysicalDisk**, **Enclosure**, or **SSU** to this cmdlet.

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-StorageMaintenanceMode](./Enable-StorageMaintenanceMode.md)

[Get-PhysicalDisk](./Get-PhysicalDisk.md)
