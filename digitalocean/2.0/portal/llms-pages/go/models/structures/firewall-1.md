# Firewall 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsMQ

An object specifying allow and deny rules to control traffic to the load balancer.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Firewall1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Allow` | `[]string` | Optional | the rules for allowing traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `Deny` | `[]string` | Optional | the rules for denying traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    firewall1 := models.Firewall1{
        Allow:                 []string{
            "ip:1.2.3.4",
            "cidr:2.3.0.0/16",
        },
        Deny:                  []string{
            "ip:1.2.3.4",
            "cidr:2.3.0.0/16",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



