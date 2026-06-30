# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RemoveFrom` | [`List<FirewallRemoveFromResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

RemoveFromResourcesRequest removeFromResourcesRequest = new RemoveFromResourcesRequest
{
    RemoveFrom = new List<FirewallRemoveFromResources>
    {
        new FirewallRemoveFromResources
        {
            LabelSelector = new LabelSelector5
            {
                Selector = "selector8",
            },
            Server = new Server9
            {
                Id = 14,
            },
            Type = Type7Enum.Server,
        },
    },
};
```



