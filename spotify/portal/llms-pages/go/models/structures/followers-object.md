# Followers Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/go/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Href` | `models.Optional[string]` | Optional | This will always be set to null, as the Web API does not support it at the moment. |
| `Total` | `*int` | Optional | The total number of followers. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    followersObject := models.FollowersObject{
        Href:                  models.NewOptional(models.ToPointer("href2")),
        Total:                 models.ToPointer(62),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



