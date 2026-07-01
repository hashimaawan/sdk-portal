# Image 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlMw

The cost of Image per GB/month

*This model accepts additional fields of type interface{}.*


# Class Name

`Image3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PricePerGbMonth` | [`models.PricePerGbMonth`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-per-gb-month.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    image3 := models.Image3{
        PricePerGbMonth:       models.PricePerGbMonth{
            Gross:                 "1.1900000000000000",
            Net:                   "1.0000000000",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



