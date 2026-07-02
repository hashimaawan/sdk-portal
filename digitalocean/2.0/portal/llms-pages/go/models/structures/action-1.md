# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Action1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `*string` | Optional | A URL that can be used to access the action. |
| `Id` | `*int` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `Rel` | `*string` | Optional | A string specifying the type of the related action. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    action1 := models.Action1{
        Href:                  models.ToPointer("https://api.digitalocean.com/v2/actions/7515"),
        Id:                    models.ToPointer(7515),
        Rel:                   models.ToPointer("create"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



