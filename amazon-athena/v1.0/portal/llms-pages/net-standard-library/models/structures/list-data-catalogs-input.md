# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 2`, `<= 50` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListDataCatalogsInput listDataCatalogsInput = new ListDataCatalogsInput
{
    NextToken = "NextToken8",
    MaxResults = 50,
};
```



