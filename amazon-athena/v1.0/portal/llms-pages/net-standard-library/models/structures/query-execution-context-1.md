# Query Execution Context 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uQ29udGV4dDE

*This model accepts additional fields of type object.*


# Class Name

`QueryExecutionContext1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Database` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `Catalog` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

QueryExecutionContext1 queryExecutionContext1 = new QueryExecutionContext1
{
    Database = "Database0",
    Catalog = "Catalog6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



