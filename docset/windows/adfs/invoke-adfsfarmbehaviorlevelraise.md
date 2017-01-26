---
author: brianlic-msft-msft
description: 
external help file: Microsoft.IdentityServer.Deployment.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Invoke-AdfsFarmBehaviorLevelRaise
ms.assetid: F34B3067-3211-4303-A295-2EB709A42A1A
---

# Invoke-AdfsFarmBehaviorLevelRaise

## SYNOPSIS
Raises the behavior level of a farm.

## SYNTAX

### AdfsUpgradeServiceAccount (Default)
```
Invoke-AdfsFarmBehaviorLevelRaise [-Member <String[]>] [-Credential <PSCredential>]
 [-ServiceAccountCredential <PSCredential>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AdfsUpgradeGmsaAccount
```
Invoke-AdfsFarmBehaviorLevelRaise [-Member <String[]>] [-Credential <PSCredential>]
 [-GroupServiceAccountIdentifier <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-AdfsFarmBehaviorLevelRaise** cmdlet raises the behavior level of an Active Directory Federation Services (AD FS) farm to enable the new features that are available in later versions of the Windows operating system.

To raise the behavior level of a farm that uses SQL Server as the policy database, specify the *Credential* parameter.

## EXAMPLES

### Example 1: Raise the farm behavior level
```
PS C:\>Invoke-AdfsFarmBehaviorLevelRaise
```

This command raises the farm behavior level from Windows Server 2012 R2 to the Windows Server 2016 level.
The command applies to the latest version available on your forest.
You not have to specify the level.

### Example 2: Raise the farm behavior level for a farm that uses SQL Server
```
PS C:\>$Credentials = Get-Credential
PS C:\> Invoke-AdfsFarmBehaviorLevelRaise -Credential $Credentials
```

The first command prompts you for user name and password by using the Get-Credential cmdlet.
The command stores the credentials in the $Credentials variable.

The second command raises the farm behavior level from Windows Server 2012 R2 to the Windows Server 2016 level.
The cmdlet specifies the necessary credentials stored in $Credentials.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifies credentials necessary to run this cmdlet for an AD FS farm that uses SQL Server as the policy database.
The credentials provided must be an administrator on each AD FS server.
To obtain a **PSCredential** object, use the Get-Credential cmdlet.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -GroupServiceAccountIdentifier
Specifies the ID of a group Managed Service Account.

```yaml
Type: String
Parameter Sets: AdfsUpgradeGmsaAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Member
Specifies an array of members.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceAccountCredential
Specifies credentials for a service account.

```yaml
Type: PSCredential
Parameter Sets: AdfsUpgradeServiceAccount
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Restore-AdfsFarmBehaviorLevel](./Restore-AdfsFarmBehaviorLevel.md)

[Test-AdfsFarmBehaviorLevelRaise](./Test-AdfsFarmBehaviorLevelRaise.md)

[Test-AdfsFarmBehaviorLevelRestore](./Test-AdfsFarmBehaviorLevelRestore.md)
