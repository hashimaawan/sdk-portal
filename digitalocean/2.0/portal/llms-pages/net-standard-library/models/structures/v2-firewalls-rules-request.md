# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InboundRules` | [`List<InboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/inbound-rule.md) | Required | - |
| `OutboundRules` | [`List<OutboundRule>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/outbound-rule.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

V2FirewallsRulesRequest v2FirewallsRulesRequest = new V2FirewallsRulesRequest
{
    InboundRules = new List<InboundRule>
    {
        new InboundRule
        {
            Ports = "8000",
            Protocol = Protocol.Tcp,
            Sources = new Sources
            {
                Addresses = new List<string>
                {
                    "1.2.3.4",
                    "18.0.0.0/8",
                },
                DropletIds = new List<int>
                {
                    8043964,
                },
                KubernetesIds = new List<string>
                {
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                },
                LoadBalancerUids = new List<string>
                {
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                },
                Tags = new List<string>
                {
                    "tags1",
                    "tags2",
                    "tags3",
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    OutboundRules = new List<OutboundRule>
    {
        new OutboundRule
        {
            Ports = "8000",
            Protocol = Protocol.Tcp,
            Destinations = new Destinations
            {
                Addresses = new List<string>
                {
                    "1.2.3.4",
                    "18.0.0.0/8",
                },
                DropletIds = new List<int>
                {
                    8043964,
                },
                KubernetesIds = new List<string>
                {
                    "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                },
                LoadBalancerUids = new List<string>
                {
                    "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                },
                Tags = new List<string>
                {
                    "tags7",
                    "tags8",
                    "tags9",
                },
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



