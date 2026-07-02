# Column Info

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbHVtbkluZm8

Information about the columns in a query execution result.

*This model accepts additional fields of type object.*


# Class Name

`ColumnInfo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Optional | - |
| `SchemaName` | `string` | Optional | - |
| `TableName` | `string` | Optional | - |
| `Name` | `string` | Required | - |
| `Label` | `string` | Optional | - |
| `Type` | `string` | Required | - |
| `Precision` | `int?` | Optional | - |
| `Scale` | `int?` | Optional | - |
| `Nullable` | [`ColumnNullable2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/column-nullable-2.md) | Optional | - |
| `CaseSensitive` | `bool?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ColumnInfo columnInfo = new ColumnInfo
{
    Name = "Name8",
    Type = "Type8",
    CatalogName = "CatalogName2",
    SchemaName = "SchemaName2",
    TableName = "TableName4",
    Label = "Label6",
    Precision = 196,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



