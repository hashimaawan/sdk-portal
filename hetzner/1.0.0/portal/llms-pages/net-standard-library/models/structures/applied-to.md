# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AppliedToResources` | [`List<AppliedToResource>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/applied-to-resource.md) | Optional | - |
| `LabelSelector` | [`LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/label-selector.md) | Optional | - |
| `Server` | [`Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/server.md) | Optional | - |
| `Type` | [`Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-6.md) | Required | Type of resource referenced |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

AppliedTo appliedTo = new AppliedTo
{
    Type = Type6Enum.Server,
    AppliedToResources = new List<AppliedToResource>
    {
        new AppliedToResource
        {
            Server = new Server
            {
                Id = 14,
            },
            Type = Type5Enum.Server,
        },
        new AppliedToResource
        {
            Server = new Server
            {
                Id = 14,
            },
            Type = Type5Enum.Server,
        },
    },
    LabelSelector = new LabelSelector
    {
        Selector = "selector8",
    },
    Server = new Server
    {
        Id = 14,
    },
};
```



