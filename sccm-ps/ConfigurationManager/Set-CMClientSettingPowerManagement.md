---
description: Sets a client setting power management.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientSettingPowerManagement
---

# Set-CMClientSettingPowerManagement

## SYNOPSIS
Sets a client setting power management.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingPowerManagement [-AllowUserToOptOutFromPowerPlan <Boolean>] [-Enable <Boolean>]
 [-EnableWakeupProxy <Boolean>] [-FirewallExceptionForWakeupProxy <WakeUpProxyFirewallExceptionTypes>]
 [-NetworkWakeupOption <NetworkWakeupType>] [-WakeOnLanPort <Int32>] [-WakeupProxyDirectAccessPrefix <String>]
 [-WakeupProxyPort <Int32>] -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingPowerManagement [-AllowUserToOptOutFromPowerPlan <Boolean>] [-Enable <Boolean>]
 [-EnableWakeupProxy <Boolean>] [-FirewallExceptionForWakeupProxy <WakeUpProxyFirewallExceptionTypes>]
 [-NetworkWakeupOption <NetworkWakeupType>] [-WakeOnLanPort <Int32>] [-WakeupProxyDirectAccessPrefix <String>]
 [-WakeupProxyPort <Int32>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingPowerManagement [-AllowUserToOptOutFromPowerPlan <Boolean>] [-Enable <Boolean>]
 [-EnableWakeupProxy <Boolean>] [-FirewallExceptionForWakeupProxy <WakeUpProxyFirewallExceptionTypes>]
 [-NetworkWakeupOption <NetworkWakeupType>] [-WakeOnLanPort <Int32>] [-WakeupProxyDirectAccessPrefix <String>]
 [-WakeupProxyPort <Int32>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example

```PowerShell
Set-CMClientSettingPowerManagement -Name "test settings" -AllowUserToOptOutFromPowerPlan $true -EnableWakeupProxy $true -NetworkWakeupOption Enabled -WakeupProxyPort 25511 -WakeOnLanPort 10 -FirewallExceptionForWakeupProxy None
```

## PARAMETERS

### -AllowUserToOptOutFromPowerPlan
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
Position: Named
Default value: None
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

### -Enable
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnablePowerManagement

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWakeupProxy
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallExceptionForWakeupProxy
```yaml
Type: WakeUpProxyFirewallExceptionTypes
Parameter Sets: (All)
Aliases: WindowsFirewallExceptionsForWakeupProxy
Accepted values: None, Public, Private, Domain

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWakeupOption
Starting in version 1906, use this parameter to enable or disable the client setting, **Allow network wake-up**.

```yaml
Type: NetworkWakeupType
Parameter Sets: (All)
Aliases:
Accepted values: NotConfigured, Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -WakeOnLanPort
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeupProxyDirectAccessPrefix
```yaml
Type: String
Parameter Sets: (All)
Aliases: IPv6PrefixesForDirectAccessOrInterveningNetworkDevices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeupProxyPort
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
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
