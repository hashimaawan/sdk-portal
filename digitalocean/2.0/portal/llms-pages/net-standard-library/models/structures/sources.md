# Sources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNvdXJjZXM

*This model accepts additional fields of type [object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md).*


# Class Name

`Sources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Addresses` | `List<string>` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. |
| `DropletIds` | `List<int>` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. |
| `KubernetesIds` | `List<string>` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. |
| `LoadBalancerUids` | `List<string>` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. |
| `Tags` | `List<string>` | Optional | - |
| `AdditionalProperties` | [`object this[string key]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/net-standard-library/models/structures/object.md) | Optional | - |


# Example

```csharp
using DigitalOceanApi.Standard.Models;
using DigitalOceanApi.Standard.Utilities;
using System.Collections.Generic;

Sources sources = new Sources
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
};
```



