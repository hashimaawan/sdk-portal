# Me Episodes Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1lJTI1MjBFcGlzb2RlcyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type interface{}.*


# Class Name

`MeEpisodesRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ids` | `[]string` | Optional | A JSON array of the [Spotify IDs](/documentation/web-api/concepts/spotify-uris-ids). <br/>A maximum of 50 items can be specified in one request. _**Note**: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored._ |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    meEpisodesRequest1 := models.MeEpisodesRequest1{
        Ids:                   []string{
            "ids5",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



