# List Databases Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNJbnB1dA


# Class Name

`ListDatabasesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CatalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 50` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListDatabasesInput listDatabasesInput = new ListDatabasesInput
{
    CatalogName = "CatalogName4",
    NextToken = "NextToken0",
    MaxResults = 50,
};
```



