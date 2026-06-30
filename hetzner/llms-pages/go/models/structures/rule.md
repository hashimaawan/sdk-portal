# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlJ1bGU


# Class Name

`Rule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `models.Optional[string]` | Optional | Description of the Rule<br><br>**Constraints**: *Maximum Length*: `255` |
| `DestinationIps` | `[]string` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |
| `Direction` | [`models.DirectionEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/direction.md) | Required | Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`. |
| `Port` | `*string` | Optional | Port or port range to which traffic will be allowed, only applicable for protocols TCP and UDP. A port range can be specified by separating two ports with a dash, e.g `1024-5000`. |
| `Protocol` | [`models.ProtocolEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/protocol.md) | Required | Type of traffic to allow |
| `SourceIps` | `[]string` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    rule := models.Rule{
        Description:          models.NewOptional(models.ToPointer("description0")),
        DestinationIps:       []string{
            "28.239.13.1/32",
            "28.239.14.0/24",
            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
        },
        Direction:            models.DirectionEnum_IN,
        Port:                 models.ToPointer("80"),
        Protocol:             models.ProtocolEnum_ESP,
        SourceIps:            []string{
            "28.239.13.1/32",
            "28.239.14.0/24",
            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
        },
    }

}
```



