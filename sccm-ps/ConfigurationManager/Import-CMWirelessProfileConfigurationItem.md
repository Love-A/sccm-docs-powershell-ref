---
description: Imports a wireless profile configuration item.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMWirelessProfileConfigurationItem
---

# Import-CMWirelessProfileConfigurationItem

## SYNOPSIS
Imports a wireless profile configuration item.

## SYNTAX

```
Import-CMWirelessProfileConfigurationItem [-Description <String>] -Name <String> -Path <String>
 [-Severity <NoncomplianceSeverity>] -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMWirelessProfileConfigurationItem** cmdlet imports an existing wireless profile item from a file.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a wireless profile configuration item
```
PS XYZ:\><?xml version="1.0"?>
<WLANProfile xmlns="https://www.microsoft.com/networking/WLAN/profile/v1">
 <name>Open-WEP</name>
 <SSIDConfig>
  <SSID>
   <hex>4E455753534944283229</hex>
   <name>NEWSSID(2)</name>
  </SSID>
  <nonBroadcast>false</nonBroadcast>
 </SSIDConfig>
 <connectionType>ESS</connectionType>
 <connectionMode>auto</connectionMode>
 <autoSwitch>true</autoSwitch>
 <MSM>
  <security>
   <authEncryption>
    <authentication>open</authentication>
    <encryption>WEP</encryption>
    <useOneX>false</useOneX>
   </authEncryption>
   <preAuthThrottle>3</preAuthThrottle>
  </security>
 </MSM>
</WLANProfile>

PS XYZ:\> Import-CMWirelessProfileConfigurationItem -Name "Wireless2" -Description "Imported wireless profile" -Path "c:\WLanProfile.xml" -SupportedPlatform (Get-CMSupportedPlatform -Name "*Windows*10*" -Fast)
```

The first section provides xml content for the wireless profile.
Save this content to "C:\WLanProfile.xml".

The command gets the supported platforms for Windows 10, and imports the wireless profile named WLanProfile.xml, naming it Wireless2.
The Windows 10 platforms are provisioned with the wireless profile.

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

### -Description
Specifies a description for the wireless profile.

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

### -Name
Specifies the name of a wireless profile.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path to the file that contains the wireless profile to import.

```yaml
Type: String
Parameter Sets: (All)
Aliases: WifiProfileXmlPath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Severity
Specifies a non-compliance severity for reports.
Valid values are:

- None
- Informational
- Warning
- Critical
- CriticalWithEvent

```yaml
Type: NoncomplianceSeverity
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Critical, CriticalWithEvent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform
Specifies the supported platform object.
The platform is provisioned with the wireless profile.
To obtain a supported platform object, use the Get-CMSupportedPlatform cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

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

### None
## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy
## NOTES

## RELATED LINKS

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[New-CMWirelessProfileConfigurationItem](New-CMWirelessProfileConfigurationItem.md)

[Set-CMWirelessProfileConfigurationItem](Set-CMWirelessProfileConfigurationItem.md)


