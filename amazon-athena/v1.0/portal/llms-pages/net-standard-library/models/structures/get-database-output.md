# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/database-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetDatabaseOutput getDatabaseOutput = new GetDatabaseOutput
{
    Database = new Database2
    {
        Name = "Name2",
        Description = "Description8",
        Parameters = new Parameters
        {
        },
    },
};
```



