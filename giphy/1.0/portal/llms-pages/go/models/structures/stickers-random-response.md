# Stickers Random Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRlN0aWNrZXJzJTI1MjBSYW5kb20lMjUyMFJlc3BvbnNl


# Class Name

`StickersRandomResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Data` | [`*models.Gif`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/gif.md) | Optional | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/meta.md) | Optional | The Meta Object contains basic information regarding the request, whether it was successful, and the response given by the API.  Check `responses` to see a description of types of response codes the API might give you under different cirumstances. |


# Example

```go
package main

import (
    "log"
    "time"
    "giphyapi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    stickersRandomResponse := models.StickersRandomResponse{
        Data:                 models.ToPointer(models.Gif{
            BitlyUrl:             models.ToPointer("bitly_url0"),
            ContentUrl:           models.ToPointer("content_url4"),
            CreateDatetime:       models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
            EmbdedUrl:            models.ToPointer("embded_url8"),
            FeaturedTags:         []string{
                "featured_tags0",
            },
        }),
        Meta:                 models.ToPointer(models.Meta{
            Msg:                  models.ToPointer("msg8"),
            ResponseId:           models.ToPointer("response_id0"),
            Status:               models.ToPointer(98),
        }),
    }

}
```



