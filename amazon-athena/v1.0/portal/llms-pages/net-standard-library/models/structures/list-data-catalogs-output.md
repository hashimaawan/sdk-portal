# List Data Catalogs Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NPdXRwdXQ


# Class Name

`ListDataCatalogsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DataCatalogsSummary` | [`List<DataCatalogSummary>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/data-catalog-summary.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ListDataCatalogsOutput listDataCatalogsOutput = new ListDataCatalogsOutput
{
    DataCatalogsSummary = new List<DataCatalogSummary>
    {
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2Enum.HIVE,
        },
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2Enum.HIVE,
        },
        new DataCatalogSummary
        {
            CatalogName = "CatalogName4",
            Type = DataCatalogType2Enum.HIVE,
        },
    },
    NextToken = "NextToken0",
};
```



