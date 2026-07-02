# Get Data Catalog Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldERhdGFDYXRhbG9nT3V0cHV0


# Class Name

`GetDataCatalogOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalog` | [`DataCatalog2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/data-catalog-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetDataCatalogOutput getDataCatalogOutput = new GetDataCatalogOutput
{
    DataCatalog = new DataCatalog2
    {
        Name = "Name4",
        Type = DataCatalogType1Enum.GLUE,
        Description = "Description2",
        Parameters = new Parameters
        {
        },
    },
};
```



