# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NumNodes` | `*int` | Optional | - |
| `Sizes` | `[]string` | Optional, Read-only | An array of objects containing the slugs available with various node counts |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    layout := models.Layout{
        NumNodes:              models.ToPointer(1),
        Sizes:                 []string{
            "db-s-1vcpu-1gb",
            "db-s-1vcpu-2gb",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



