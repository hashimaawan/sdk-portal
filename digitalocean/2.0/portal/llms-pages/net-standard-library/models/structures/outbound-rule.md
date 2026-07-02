# Outbound Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk91dGJvdW5kUnVsZQ

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`OutboundRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ports` | `string` | Required | The ports on which traffic will be allowed specified as a string containing a single port, a range (e.g. "8000-9000"), or "0" when all ports are open for a protocol. For ICMP rules this parameter will always return "0". |
| `Protocol` | [`Protocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/enumerations/protocol.md) | Required | The type of traffic to be allowed. This may be one of `tcp`, `udp`, or `icmp`. |
| `Destinations` | [`Destinations`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/destinations.md) | Required | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

OutboundRule outboundRule = new OutboundRule
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
};
```



