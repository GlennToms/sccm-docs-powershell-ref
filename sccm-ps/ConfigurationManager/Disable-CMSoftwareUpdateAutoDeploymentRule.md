<<<<<<< HEAD
---
title: Disable-CMSoftwareUpdateAutoDeploymentRule
titleSuffix: Configuration Manager
description: Disables Configuration Manager deployment rules for automatic software updates.
ms.date: 05/01/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: A1766572-846D-47B8-A9C9-01745BB7E114
online version: https://go.microsoft.com/fwlink/?linkid=833957
schema: 2.0.0
>>>>>>> master
---

# Disable-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Disables Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByIdMandatory (Default)
```
Disable-CMSoftwareUpdateAutoDeploymentRule -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Disable-CMSoftwareUpdateAutoDeploymentRule -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMSoftwareUpdateAutoDeploymentRule** cmdlet disables specified Microsoft System Center Configuration Manager deployment rules for automatic software updates.
While a rule is disabled, it does not run in accordance with its schedule and you cannot run it manually.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules to disable by ID or by name, or specify a rule object by using the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.
You can use the [Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet to enable a rule.
To remove a rule permanently, use the [Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Disable a deployment rule by name
```
PS XYZ:\>Disable-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
```

This command disables a rule named Weekly Driver Updates.

### Example 2: Disable a deployment rule by ID
```
PS XYZ:\>Disable-CMSoftwareUpdateAutoDeploymentRule -Id "16777217"
```

This command disables a deployment rule that has the ID 16777217.

### Example 3: Disable a deployment rule by using a variable
```
PS XYZ:\> $CMSUADR = Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
PS XYZ:\> Disable-CMSoftwareUpdateAutoDeploymentRule -InputObject $CMSUADR
```

The first command gets a deployment rule that has the specified name, and then stores it in the $CMSUADR variable.

The second command disables the rule stored in the variable.

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

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -Id
Specifies an array of IDs for rules for automatic deployment of software updates.
This value is the **AutoDeploymentID** property of the deployment rule object.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update automatic deployment rule object.
To obtain a deployment rule object, use **Get-CMSoftwareUpdateAutoDeploymentRule**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a rule for automatic deployment of software updates.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
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

[Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](Set-CMSoftwareUpdateAutoDeploymentRule.md)


