# Stickers Search Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBTZWFyY2glMjUyMFJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`StickersSearchResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`[]models.Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/gif.md) | Optional | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |
| `Pagination` | [`*models.Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/pagination.md) | Optional | The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "giphyApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    stickersSearchResponse := models.StickersSearchResponse{
        Data:                  []models.Gif{
            models.Gif{
                BitlyUrl:              models.ToPointer("bitly_url0"),
                ContentUrl:            models.ToPointer("content_url4"),
                CreateDatetime:        models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                EmbdedUrl:             models.ToPointer("embded_url8"),
                FeaturedTags:          []string{
                    "featured_tags0",
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Meta:                  models.ToPointer(models.Meta{
            Msg:                   models.ToPointer("msg8"),
            ResponseId:            models.ToPointer("response_id0"),
            Status:                models.ToPointer(98),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Pagination:            models.ToPointer(models.Pagination{
            Count:                 models.ToPointer(192),
            Offset:                models.ToPointer(240),
            TotalCount:            models.ToPointer(100),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



