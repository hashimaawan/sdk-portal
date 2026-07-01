# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJ1bGU


# Class Name

`Rule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | Description of the Rule<br><br>**Constraints**: *Maximum Length*: `255` |
| `DestinationIps` | `List<string>` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |
| `Direction` | [`DirectionEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/direction.md) | Required | Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`. |
| `Port` | `string` | Optional | Port or port range to which traffic will be allowed, only applicable for protocols TCP and UDP. A port range can be specified by separating two ports with a dash, e.g `1024-5000`. |
| `Protocol` | [`ProtocolEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/protocol.md) | Required | Type of traffic to allow |
| `SourceIps` | `List<string>` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using System.Collections.Generic;

Rule rule = new Rule
{
    Direction = DirectionEnum.In,
    Protocol = ProtocolEnum.Esp,
    Description = "description0",
    DestinationIps = new List<string>
    {
        "28.239.13.1/32",
        "28.239.14.0/24",
        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
    },
    Port = "80",
    SourceIps = new List<string>
    {
        "28.239.13.1/32",
        "28.239.14.0/24",
        "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
    },
};
```



