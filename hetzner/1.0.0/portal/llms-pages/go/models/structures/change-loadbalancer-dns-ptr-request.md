# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DnsPtr` | `*string` | Required | Hostname to set as a reverse DNS PTR entry |
| `Ip` | `string` | Required | Public IP address for which the reverse DNS entry should be set |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    changeLoadbalancerDnsPtrRequest := models.ChangeLoadbalancerDnsPtrRequest{
        DnsPtr:                models.ToPointer("lb1.example.com"),
        Ip:                    "1.2.3.4",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



