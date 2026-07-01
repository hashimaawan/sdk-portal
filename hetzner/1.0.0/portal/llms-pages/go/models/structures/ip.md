# Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklw

IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well.

*This model accepts additional fields of type interface{}.*


# Class Name

`Ip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ip` | `string` | Required | IP of a server that belongs to the same customer (public IPv4/IPv6) or private IP in a Subnetwork type vswitch. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    ip := models.Ip{
        Ip:                    "203.0.113.1",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



