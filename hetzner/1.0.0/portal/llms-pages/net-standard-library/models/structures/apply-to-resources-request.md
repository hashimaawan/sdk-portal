# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`List<FirewallApplyToResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

ApplyToResourcesRequest applyToResourcesRequest = new ApplyToResourcesRequest
{
    ApplyTo = new List<FirewallApplyToResources>
    {
        new FirewallApplyToResources
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



