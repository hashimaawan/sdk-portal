# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | [`Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/database-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

GetDatabaseOutput getDatabaseOutput = new GetDatabaseOutput
{
    Database = new Database2
    {
        Name = "Name2",
        Description = "Description8",
        Parameters = new Parameters
        {
            ["exampleAdditionalProperty"] = "Parameters_additionalProperties2",
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



