---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# Remove-CMTSStepApplyNetworkSetting

## SYNOPSIS

Remove the **Apply Network Settings** step from a task sequence.

## SYNTAX

### ByValue (Default)
```
Remove-CMTSStepApplyNetworkSetting [-InputObject] <IResultObject> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMTSStepApplyNetworkSetting [-TaskSequenceId] <String> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMTSStepApplyNetworkSetting [-TaskSequenceName] <String> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove an instance of the **Apply Network Settings** step from a task sequence.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a task sequence object in the **$tsOsd** variable. It then passes that variable as the input object to remove the **Apply Network Settings** step.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNameApplyNetSet = "Apply Network Settings"
Remove-CMTSStepApplyNetworkSetting -InputObject $tsOsd -StepName $tsStepNameApplyNetSet -Force
```

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

### -InputObject

Specify a task sequence object from which to remove the **Apply Network Settings** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specify the name of the **Apply Network Settings** step to remove from the task sequence.

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

### -TaskSequenceId

Specify the **package ID** of the task sequence from which to remove the **Apply Network Settings** step. This value is a standard package ID, for example `XYZ00858`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name of the task sequence from which to remove the **Apply Network Settings** step.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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
Default value: None
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

[Get-CMTSStepApplyNetworkSetting](Get-CMTSStepApplyNetworkSetting.md)
[New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md)
[Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[About task sequence steps: Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings)
