# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkRuc1B0cjg

*This model accepts additional fields of type interface{}.*


# Class Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `Ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    dnsPtr8 := models.DnsPtr8{
        DnsPtr:                "server.example.com",
        Ip:                    "2001:db8::1",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



