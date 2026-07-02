# List Table Metadata Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhSW5wdXQ


# Class Name

`ListTableMetadataInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `DatabaseName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Expression` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `256` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListTableMetadataInput listTableMetadataInput = new ListTableMetadataInput
{
    CatalogName = "CatalogName2",
    DatabaseName = "DatabaseName2",
    Expression = "Expression0",
    NextToken = "NextToken8",
    MaxResults = 50,
};
```



