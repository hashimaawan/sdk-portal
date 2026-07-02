# Sticky Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlN0aWNreVNlc3Npb25z

An object specifying sticky sessions settings for the load balancer.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`StickySessions`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CookieName` | `*string` | Optional | The name of the cookie sent to the client. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `CookieTtlSeconds` | `*int` | Optional | The number of seconds until the cookie set by the load balancer expires. This attribute is only returned when using `cookies` for the sticky sessions type. |
| `Type` | [`*models.Type16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/type-16.md) | Optional | An attribute indicating how and if requests from a client will be persistently served by the same backend Droplet. The possible values are `cookies` or `none`.<br><br>**Default**: `"none"` |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    stickySessions := models.StickySessions{
        CookieName:            models.ToPointer("DO-LB"),
        CookieTtlSeconds:      models.ToPointer(300),
        Type:                  models.ToPointer(models.Type16_Cookies),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



