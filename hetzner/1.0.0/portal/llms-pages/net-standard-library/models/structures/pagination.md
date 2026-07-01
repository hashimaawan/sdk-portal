# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlBhZ2luYXRpb24


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LastPage` | `double?` | Required | ID of the last page available. Can be null if the current page is the last one. |
| `NextPage` | `double?` | Required | ID of the next page. Can be null if the current page is the last one. |
| `Page` | `double` | Required | Current page number |
| `PerPage` | `double` | Required | Maximum number of items shown per page in the response |
| `PreviousPage` | `double?` | Required | ID of the previous page. Can be null if the current page is the first one. |
| `TotalEntries` | `double?` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Pagination pagination = new Pagination
{
    LastPage = 4,
    NextPage = 4,
    Page = 3,
    PerPage = 25,
    PreviousPage = 2,
    TotalEntries = 100,
};
```



