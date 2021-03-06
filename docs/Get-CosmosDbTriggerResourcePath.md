---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# Get-CosmosDbTriggerResourcePath

## SYNOPSIS

Return the resource path for a trigger object.

## SYNTAX

```powershell
Get-CosmosDbTriggerResourcePath [-Database] <String> [-CollectionId] <String> [-Id] <String>
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet returns the resource identifier for a
trigger object.

## EXAMPLES

### Example 1

```powershell
PS C:\> Get-CosmosDbTriggerResourcePath -Database 'MyDatabase' -CollectionId 'MyCollection' -Id 'sp_batch'
```

Generate a resource path for trigger with Id 'mytrigger'
in collection 'MyCollection' in database 'MyDatabase'.

## PARAMETERS

### -CollectionId

This is the Id of the collection containing the trigger.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

This is the database containing the trigger.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id

This is the Id of the trigger.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.String

## NOTES

## RELATED LINKS
