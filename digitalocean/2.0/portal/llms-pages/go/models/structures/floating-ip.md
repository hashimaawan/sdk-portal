# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cost` | `*string` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. |
| `Id` | `*string` | Optional | The unique identifier for the resource associated with the Droplet. |
| `Name` | `*string` | Optional | The name of the resource associated with the Droplet. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    floatingIp := models.FloatingIp{
        Cost:                  models.ToPointer("0.05"),
        Id:                    models.ToPointer("61486916"),
        Name:                  models.ToPointer("ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



