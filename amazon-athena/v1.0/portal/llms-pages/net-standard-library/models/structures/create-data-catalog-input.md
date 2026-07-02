# Create Data Catalog Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZURhdGFDYXRhbG9nSW5wdXQ


# Class Name

`CreateDataCatalogInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Type` | [`DataCatalogType1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/data-catalog-type-1.md) | Required | - |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/parameters.md) | Optional | - |
| `Tags` | [`List<Tag>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/tag.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

CreateDataCatalogInput createDataCatalogInput = new CreateDataCatalogInput
{
    Name = "Name6",
    Type = DataCatalogType1Enum.GLUE,
    Description = "Description2",
    Parameters = new Parameters
    {
    },
    Tags = new List<Tag>
    {
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
        new Tag
        {
            Key = "Key0",
            MValue = "Value6",
        },
    },
};
```



