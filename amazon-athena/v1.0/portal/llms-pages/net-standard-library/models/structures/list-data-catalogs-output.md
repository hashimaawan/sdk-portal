# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalogsSummary` | [`List<DataCatalogSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/data-catalog-summary.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ListDataCatalogsOutput listDataCatalogsOutput = new ListDataCatalogsOutput
{
    DataCatalogsSummary = new List<DataCatalogSummary>
    {
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2.Hive,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2.Hive,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2.Hive,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    NextToken = "NextToken0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



