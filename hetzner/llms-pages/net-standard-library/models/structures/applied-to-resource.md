# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/server.md) | Optional | - |
| `Type` | [`Type5Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-5.md) | Optional | Type of resource referenced |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

AppliedToResource appliedToResource = new AppliedToResource
{
    Server = new Server
    {
        Id = 14,
    },
    Type = Type5Enum.Server,
};
```



