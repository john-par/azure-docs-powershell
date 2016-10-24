---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
online version: de6e6b3c-ca2c-417c-93fe-d705cf72b5f6
schema: 2.0.0
ms.assetid: 71357C7C-C3F4-44ED-8DCA-954025179A67
---

# Unregister-AzureRmRecoveryServicesBackupContainer

## SYNOPSIS
Unregisters a Windows Server or other container from the vault.

## SYNTAX

```
Unregister-AzureRmRecoveryServicesBackupContainer [-Container] <ContainerBase> [<CommonParameters>]
```

## DESCRIPTION
The **Unregister-AzureRmRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.
This cmdlet removes references to a container from the vault.
Before you can unregister a container, you must delete any protected data associated with that container.

Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.

## EXAMPLES

### Example 1: Unregister a Windows Server from the vault
```
PS C:\>$Cont = Get-AzureRmRecoveryServicesContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServiceBackupContainer -Container $Cont
```

The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.

The second command unregisters the specified Windows Server from the Azure Backup vault.

## PARAMETERS

### -Container
Specifies a Backup container object to unregister.
To obtain a **BackupContainer** object, use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.

```yaml
Type: ContainerBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmRecoveryServicesBackupContainer](.\Get-AzureRmRecoveryServicesBackupContainer.md)

