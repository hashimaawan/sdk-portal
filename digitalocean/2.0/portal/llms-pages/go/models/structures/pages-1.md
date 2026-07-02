# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `First` | `*string` | Optional | URI of the first page of the results. |
| `Prev` | `*string` | Optional | URI of the previous page of the results. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    pages1 := models.Pages1{
        First:                 models.ToPointer("https://api.digitalocean.com/v2/images?page=1"),
        Prev:                  models.ToPointer("https://api.digitalocean.com/v2/images?page=1"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



