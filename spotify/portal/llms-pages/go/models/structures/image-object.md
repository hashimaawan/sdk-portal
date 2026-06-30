# Image Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkltYWdlT2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ImageObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Url` | `string` | Required | The source URL of the image. |
| `Height` | `*int` | Required | The image height in pixels. |
| `Width` | `*int` | Required | The image width in pixels. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    imageObject := models.ImageObject{
        Url:                   "https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n",
        Height:                models.ToPointer(300),
        Width:                 models.ToPointer(300),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



