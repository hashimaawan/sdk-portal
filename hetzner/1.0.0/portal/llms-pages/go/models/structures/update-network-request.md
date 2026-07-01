# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0

*This model accepts additional fields of type interface{}.*


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`*models.Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `*string` | Optional | New network name |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    updateNetworkRequest := models.UpdateNetworkRequest{
        Labels:                models.ToPointer(models.Labels2{
            Labelkey:              models.ToPointer("labelkey4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Name:                  models.ToPointer("new-name"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



