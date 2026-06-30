# Track 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlRyYWNrMQ

*This model accepts additional fields of type interface{}.*


# Class Name

`Track1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Uri` | `*string` | Optional | Spotify URI |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    track1 := models.Track1{
        Uri:                   models.ToPointer("uri0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



