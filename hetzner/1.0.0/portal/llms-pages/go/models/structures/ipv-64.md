# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry

*This model accepts additional fields of type interface{}.*


# Class Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blocked` | `bool` | Required | If the IP is blocked by our anti abuse dept |
| `DnsPtr` | [`[]models.DnsPtr8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `Id` | `*int` | Optional | ID of the Resource |
| `Ip` | `string` | Required | IP address (v6) of this Server |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    ipv64 := models.Ipv64{
        Blocked:               false,
        DnsPtr:                []models.DnsPtr8{
            models.DnsPtr8{
                DnsPtr:                "server.example.com",
                Ip:                    "2001:db8::1",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Id:                    models.ToPointer(42),
        Ip:                    "2001:db8::/64",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



