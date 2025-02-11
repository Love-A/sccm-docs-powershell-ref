---
description: Removes Configuration Manager software update groups.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMSoftwareUpdateGroup
---

# Remove-CMSoftwareUpdateGroup

## SYNOPSIS
Removes Configuration Manager software update groups.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMSoftwareUpdateGroup [-Force] -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMSoftwareUpdateGroup [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareUpdateGroup [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSoftwareUpdateGroup** cmdlet removes software update groups from Configuration Manager.
You can specify each software update group that you are removing by using the group IDs or names.
If you remove a software update group, you can use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet to return a software update group object and use that object to specify the group that you want to remove.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a software update group by using an ID
```
PS XYZ:\> Remove-CMSoftwareUpdateGroup -Id "ST10000B"
```

This command removes the software update group that has the ID ST10000B.

### Example 2: Remove a software update group by using a name
```
PS XYZ:\> Remove-CMSoftwareUpdateGroup -Name "SUGroupD01"
```

This command removes the software update group named SUGroupD01.

### Example 3: Remove a software update group by using an object variable
```
PS XYZ:\> $SubObj=Get-CMSoftwareUpdateGroup -Id "ST10000B"
PS XYZ:\> Remove-CMSoftwareUpdateGroup -SoftwareUpdateGroup $SubObj
```

The first command gets the software update group that has the ID ST10000B, and then stores it in the variable $SubObj.

The second command removes the software update group by using the $SubObj variable.

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

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
Specifies an array of software update group IDs.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the software update group object to remove.
To obtain a software update group object, use **Get-CMSoftwareUpdateGroup**.

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
Specifies an array of software update group names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[New-CMSoftwareUpdateGroup](New-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateGroup](Set-CMSoftwareUpdateGroup.md)


