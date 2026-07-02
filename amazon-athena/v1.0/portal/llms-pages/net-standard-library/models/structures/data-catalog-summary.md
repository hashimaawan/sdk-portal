# Data Catalog Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRhdGFDYXRhbG9nU3VtbWFyeQ

The summary information for the data catalog, which includes its name and type.

*This model accepts additional fields of type object.*


# Class Name

`DataCatalogSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Type` | [`DataCatalogType2?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/data-catalog-type-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

DataCatalogSummary dataCatalogSummary = new DataCatalogSummary
{
    CatalogName = "CatalogName2",
    Type = DataCatalogType2.Hive,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



