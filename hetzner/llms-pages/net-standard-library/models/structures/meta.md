# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRk1ldGE


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/pagination.md) | Required | - |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

Meta meta = new Meta
{
    Pagination = new Pagination
    {
        LastPage = 4,
        NextPage = 4,
        Page = 3,
        PerPage = 25,
        PreviousPage = 2,
        TotalEntries = 100,
    },
};
```



