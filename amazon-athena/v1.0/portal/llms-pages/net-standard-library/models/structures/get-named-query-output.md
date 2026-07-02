# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQuery` | [`NamedQuery1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/named-query-1.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

GetNamedQueryOutput getNamedQueryOutput = new GetNamedQueryOutput
{
    NamedQuery = new NamedQuery1
    {
        Name = "Name0",
        Database = "Database8",
        QueryString = "QueryString2",
        Description = "Description6",
        NamedQueryId = "NamedQueryId2",
        WorkGroup = "WorkGroup2",
    },
};
```



