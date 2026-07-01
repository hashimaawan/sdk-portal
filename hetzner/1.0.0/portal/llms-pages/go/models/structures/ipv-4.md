# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)

*This model accepts additional fields of type interface{}.*


# Class Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `models.Optional[string]` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `Ip` | `models.Optional[string]` | Optional | IP address (v4) of this Load Balancer |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    ipv4 := models.Ipv4{
        DnsPtr:                models.NewOptional(models.ToPointer("lb1.example.com")),
        Ip:                    models.NewOptional(models.ToPointer("1.2.3.4")),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



