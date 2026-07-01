# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkRuc1B0cg

*This model accepts additional fields of type interface{}.*


# Class Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv4 or IPv6 address |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    dnsPtr := models.DnsPtr{
        DnsPtr:                "server.example.com",
        Ip:                    "2001:db8::1",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



