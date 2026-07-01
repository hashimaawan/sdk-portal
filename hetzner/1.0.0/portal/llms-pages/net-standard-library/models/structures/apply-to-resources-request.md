# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`List<FirewallApplyToResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Server = new Server9
            {
                Id = 14,
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            Type = Type7.Server,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



