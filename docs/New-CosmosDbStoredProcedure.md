---
external help file: CosmosDB-help.xml
Module Name: CosmosDB
online version:
schema: 2.0.0
---

# New-CosmosDbStoredProcedure

## SYNOPSIS

Create a new stored procedure for a collection in a Cosmos DB database.

## SYNTAX

### Context (Default)

```powershell
New-CosmosDbStoredProcedure -Context <Context> [-KeyType <String>] [-Key <SecureString>] [-Database <String>]
 -CollectionId <String> -Id <String> -StoredProcedureBody <String> [<CommonParameters>]
```

### Account

```powershell
New-CosmosDbStoredProcedure -Account <String> [-KeyType <String>] [-Key <SecureString>] [-Database <String>]
 -CollectionId <String> -Id <String> -StoredProcedureBody <String> [<CommonParameters>]
```

## DESCRIPTION

This cmdlet will create a stored procedure for a collection in a Cosmos DB.

## EXAMPLES

### Example 1

```powershell
PS C:\> $Body = @'
function (personToGreet) {
    var context = getContext();
    var response = context.getResponse();

    response.setBody("Hello, " + personToGreet);
}
'@
PS C:\> New-CosmosDbStoredProcedure -Context $cosmosDbContext -CollectionId 'MyNewCollection' -Id 'spHelloWorld' -StoredProcedureBody $Body
```

Create a stored procedure 'spHelloWorld' in a collection in the database.

## PARAMETERS

### -Account

The account name of the Cosmos DB to access.

```yaml
Type: String
Parameter Sets: Account
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

This is the Id of the collection to create the stored procedure for.

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

### -Context

This is an object containing the context information of the Cosmos DB database
that will be deleted. It should be created by \`New-CosmosDbContext\`.

```yaml
Type: Context
Parameter Sets: Context
Aliases: Connection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database

The name of the database to access in the Cosmos DB account.

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

### -Id

This is the Id of the stored procedure to create.

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

### -Key

The key to be used to access this Cosmos DB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType

The type of key that will be used to access ths Cosmos DB.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: master, resource

Required: False
Position: Named
Default value: Master
Accept pipeline input: False
Accept wildcard characters: False
```

### -StoredProcedureBody

This is the body of the stored procedure.

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

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
