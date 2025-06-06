---
description: Use this topic to help manage Windows and Windows Server technologies with Windows PowerShell.
external help file: Microsoft.ActiveDirectory.Management.dll-Help.xml
Module Name: ActiveDirectory
ms.date: 12/27/2016
online version: https://learn.microsoft.com/powershell/module/activedirectory/new-adauthenticationpolicysilo?view=windowsserver2016-ps&wt.mc_id=ps-gethelp
schema: 2.0.0
title: New-ADAuthenticationPolicySilo
---

# New-ADAuthenticationPolicySilo

## SYNOPSIS
Creates an Active Directory Domain Services authentication policy silo object.

## SYNTAX

```
New-ADAuthenticationPolicySilo [-WhatIf] [-Confirm] [-AuthType <ADAuthType>]
 [-ComputerAuthenticationPolicy <ADAuthenticationPolicy>] [-Credential <PSCredential>] [-Description <String>]
 [-Enforce] [-Instance <ADAuthenticationPolicySilo>] [-Name] <String> [-OtherAttributes <Hashtable>]
 [-PassThru] [-ProtectedFromAccidentalDeletion <Boolean>] [-Server <String>]
 [-ServiceAuthenticationPolicy <ADAuthenticationPolicy>] [-UserAuthenticationPolicy <ADAuthenticationPolicy>]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-ADAuthenticationPolicySilo** cmdlet creates an authentication policy silo object in Active Directory® Domain Services.

## EXAMPLES

### Example 1: Create an authentication policy silo and enforce it
```
PS C:\> New-ADAuthenticationPolicySilo -Name AuthenticationPolicySilo01 -Enforce
```

This command creates an authentication policy silo object and enforces it.

### Example 2: Create an authentication policy silo without enforcement
```
PS C:\> New-ADAuthenticationPolicySilo -Name AuthenticationPolicySilo02
```

This command creates an authentication policy silo object but does not enforce it.

## PARAMETERS

### -AuthType
Specifies the authentication method to use.
The acceptable values for this parameter are:

- Negotiate or 0
- Basic or 1

The default authentication method is Negotiate.
A Secure Sockets Layer (SSL) connection is required for the Basic authentication method.

```yaml
Type: ADAuthType
Parameter Sets: (All)
Aliases:
Accepted values: Negotiate, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerAuthenticationPolicy
Specifies the authentication policy that applies to computer accounts.

```yaml
Type: ADAuthenticationPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Credential
Specifies a user account that has permission to perform the task.
The default is the current user.
Type a user name, such as User01 or Domain01\User01, or enter a **PSCredential** object, such as one generated by the **Get-Credential** cmdlet.

By default, the cmdlet uses the credentials of the currently logged on user unless the cmdlet is run from an Active Directory Domain Services Windows PowerShell provider drive.
If you run the cmdlet in a provider drive, the account associated with the drive is the default.

If you specify credentials that do not have permission to perform the task, the cmdlet returns an error.

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

### -Description
Specifies a description for the object.
This parameter sets the value of the description property for the object.
The Lightweight Directory Access Protocol (LDAP) display name (**ldapDisplayName**) for this property is description.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Enforce
Indicates that the authentication policy silo is enforced.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Instance
Specifies an instance of an **ADAuthenticationPolicySilo** object to use as a template for a new **ADAuthenticationPolicySilo** object.
To get the **ADAuthenticationPolicySilo** object to use as a template, use the Get-ADAuthenticationPolicySilo cmdlet.

```yaml
Type: ADAuthenticationPolicySilo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the object.
This parameter sets the **Name** property of the Active Directory Domain Services object.
The LDAP display name (**ldapDisplayName**) of this property is name.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OtherAttributes
Specifies a list of object attribute values for attributes that are not represented by other parameters.
You can set one or more attributes at the same time with this parameter, and if an attribute takes more than one value you can assign multiple values.
To identify an attribute, specify the LDAP display name (**ldapDisplayName**) defined for it in the Active Directory Domain Services schema.

Specify the attribute and the value of the attribute in the following format: @{'AttributeLDAPDisplayName'=value}.

To specify multiple values for an attribute, specify a comma separated list the values for the display name.
You can specify values for more than one attribute by using semicolons to separate attribute value pairs.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -ProtectedFromAccidentalDeletion
Indicates whether to prevent the object from being deleted.
When this property is set to true, you cannot delete the corresponding object without changing the value of the property.
The acceptable values for this parameter are:

- $False or 0
- $True or 1

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Server
Specifies the Active Directory Domain Services instance to which to connect, by providing one of the following values for a corresponding domain name or directory server.
The service may be any of the following:  Active Directory Lightweight Domain Services, Active Directory Domain Services or Active Directory snapshot instance.

Specify the Active Directory Domain Services instance in one of the following ways:

Domain name values:

- Fully qualified domain name
- NetBIOS name

Directory server values:

- Fully qualified directory server name
- NetBIOS name
- Fully qualified directory server name and port

The default value for this parameter is determined by one of the following methods in the order that they are listed:

- By using the *Server* value from objects passed through the pipeline
- By using the server information associated with the Active Directory Domain Services Windows PowerShell provider drive, when the cmdlet runs in that drive
- By using the domain of the computer running Windows PowerShell

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

### -ServiceAuthenticationPolicy
Specifies the authentication policy that applies to managed service accounts.

```yaml
Type: ADAuthenticationPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UserAuthenticationPolicy
Specifies the authentication policy that applies to user accounts.

```yaml
Type: ADAuthenticationPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ActiveDirectory.Management.ADAuthenticationPolicy

### System.String

### System.Management.Automation.SwitchParameter

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-ADAuthenticationPolicySilo](./Get-ADAuthenticationPolicySilo.md)

[Remove-ADAuthenticationPolicySilo](./Remove-ADAuthenticationPolicySilo.md)

[Set-ADAuthenticationPolicySilo](./Set-ADAuthenticationPolicySilo.md)

[AD DS Administration Cmdlets in Windows PowerShell](./activedirectory.md)
