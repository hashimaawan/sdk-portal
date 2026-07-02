# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `*int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `LastTaggedUri` | `*string` | Optional | The URI for the last tagged object for this type of resource. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    databases := models.Databases{
        Count:                 models.ToPointer(5),
        LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/images/7555620"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



