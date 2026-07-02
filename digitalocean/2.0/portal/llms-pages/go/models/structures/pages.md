# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Last` | `*string` | Optional | URI of the last page of the results. |
| `Next` | `*string` | Optional | URI of the next page of the results. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pages := models.Pages{
        Last:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=2"),
        Next:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=2"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



