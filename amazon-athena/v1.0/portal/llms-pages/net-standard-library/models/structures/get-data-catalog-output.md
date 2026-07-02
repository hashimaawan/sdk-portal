# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/data-catalog-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

GetDataCatalogOutput getDataCatalogOutput = new GetDataCatalogOutput
{
    DataCatalog = new DataCatalog2
    {
        Name = "Name4",
        Type = DataCatalogType1.Glue,
        Description = "Description2",
        Parameters = new Parameters
        {
            ["exampleAdditionalProperty"] = "Parameters_additionalProperties2",
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



