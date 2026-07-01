# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklwdjY

IP address (v6)

*This model accepts additional fields of type interface{}.*


# Class Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `models.Optional[string]` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `Ip` | `models.Optional[string]` | Optional | IP address (v6) of this Load Balancer |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    ipv6 := models.Ipv6{
        DnsPtr:                models.NewOptional(models.ToPointer("lb1.example.com")),
        Ip:                    models.NewOptional(models.ToPointer("2001:db8::1")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



