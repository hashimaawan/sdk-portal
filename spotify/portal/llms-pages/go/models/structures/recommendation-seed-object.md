# Recommendation Seed Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/go/x-redirect/JTI0bSUyRlJlY29tbWVuZGF0aW9uU2VlZE9iamVjdA

*This model accepts additional fields of type interface{}.*


# Class Name

`RecommendationSeedObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AfterFilteringSize` | `*int` | Optional | The number of tracks available after min\_\* and max\_\* filters have been applied. |
| `AfterRelinkingSize` | `*int` | Optional | The number of tracks available after relinking for regional availability. |
| `Href` | `*string` | Optional | A link to the full track or artist data for this seed. For tracks this will be a link to a Track Object. For artists a link to an Artist Object. For genre seeds, this value will be `null`. |
| `Id` | `*string` | Optional | The id used to select this seed. This will be the same as the string used in the `seed_artists`, `seed_tracks` or `seed_genres` parameter. |
| `InitialPoolSize` | `*int` | Optional | The number of recommended tracks available for this seed. |
| `Type` | `*string` | Optional | The entity type of this seed. One of `artist`, `track` or `genre`. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    recommendationSeedObject := models.RecommendationSeedObject{
        AfterFilteringSize:    models.ToPointer(118),
        AfterRelinkingSize:    models.ToPointer(194),
        Href:                  models.ToPointer("href0"),
        Id:                    models.ToPointer("id8"),
        InitialPoolSize:       models.ToPointer(124),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



