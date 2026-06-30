# Resume Point Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRlJlc3VtZVBvaW50T2JqZWN0

*This model accepts additional fields of type interface{}.*


# Class Name

`ResumePointObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FullyPlayed` | `*bool` | Optional | Whether or not the episode has been fully played by the user. |
| `ResumePositionMs` | `*int` | Optional | The user's most recent position in the episode in milliseconds. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    resumePointObject := models.ResumePointObject{
        FullyPlayed:           models.ToPointer(false),
        ResumePositionMs:      models.ToPointer(106),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



