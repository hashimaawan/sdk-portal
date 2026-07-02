# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Links`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pages` | [`*models.LinksPages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/oneof-anyof-definitions/links-pages.md) | Optional | This is a container for any-of cases. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    links := models.Links{
        Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
            Last:                  models.ToPointer("last6"),
            Next:                  models.ToPointer("next2"),
            AdditionalProperties:  map[string]interface{}{
                "pages": interface{}("[first, https://api.digitalocean.com/v2/account/keys?page=1][prev, https://api.digitalocean.com/v2/account/keys?page=2]"),
            },
        })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



