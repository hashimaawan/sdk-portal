# Me Shows Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/go/x-redirect/JTI0bSUyRk1lJTI1MjBTaG93cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`MeShowsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ids` | `[]string` | Optional | A JSON array of the [Spotify IDs](https://developer.spotify.com/documentation/web-api/#spotify-uris-and-ids).  <br>A maximum of 50 items can be specified in one request. *Note: if the `ids` parameter is present in the query string, any IDs listed here in the body will be ignored.* |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "spotifyWebApiWithFixesAndImprovementsFromSonallux/models"
)

func main() {
    meShowsRequest := models.MeShowsRequest{
        Ids:                   []string{
            "ids7",
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



