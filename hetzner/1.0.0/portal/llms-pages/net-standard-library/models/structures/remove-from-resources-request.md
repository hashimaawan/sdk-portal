# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `RemoveFrom` | [`List<FirewallRemoveFromResources>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;
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



