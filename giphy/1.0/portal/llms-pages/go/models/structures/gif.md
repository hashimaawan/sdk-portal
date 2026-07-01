# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRkdpZg


# Class Name

`Gif`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BitlyUrl` | `*string` | Optional | The unique bit.ly URL for this GIF |
| `ContentUrl` | `*string` | Optional | Currently unused |
| `CreateDatetime` | `*time.Time` | Optional | The date this GIF was added to the GIPHY database. |
| `EmbdedUrl` | `*string` | Optional | A URL used for embedding this GIF |
| `FeaturedTags` | `[]string` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) |
| `Id` | `*string` | Optional | This GIF's unique ID |
| `Images` | [`*models.Images`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. |
| `ImportDatetime` | `*time.Time` | Optional | The creation or upload date from this GIF's source. |
| `Rating` | `*string` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R |
| `Slug` | `*string` | Optional | The unique slug used in this GIF's URL |
| `Source` | `*string` | Optional | The page on which this GIF was found |
| `SourcePostUrl` | `*string` | Optional | The URL of the webpage on which this GIF was found. |
| `SourceTld` | `*string` | Optional | The top level domain of the source URL. |
| `Tags` | `[]string` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) |
| `TrendingDatetime` | `*time.Time` | Optional | The date on which this gif was marked trending, if applicable. |
| `Type` | [`*models.TypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `"gif"` |
| `UpdateDatetime` | `*time.Time` | Optional | The date on which this GIF was last updated. |
| `Url` | `*string` | Optional | The unique URL for this GIF |
| `User` | [`*models.User`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. |
| `Username` | `*string` | Optional | The username this GIF is attached to, if applicable |


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
    gif := models.Gif{
        BitlyUrl:             models.ToPointer("http://gph.is/1gsWDcL"),
        ContentUrl:           models.ToPointer("content_url4"),
        CreateDatetime:       models.ToPointer(parseTime(time.RFC3339, "2013-08-01 12:41:48", func(err error) { log.Fatalln(err) })),
        EmbdedUrl:            models.ToPointer("http://giphy.com/embed/YsTs5ltWtEhnq"),
        FeaturedTags:         []string{
            "featured_tags0",
        },
        Id:                   models.ToPointer("YsTs5ltWtEhnq"),
        ImportDatetime:       models.ToPointer(parseTime(time.RFC3339, "2013-08-01 12:41:48", func(err error) { log.Fatalln(err) })),
        Rating:               models.ToPointer("g"),
        Slug:                 models.ToPointer("confused-flying-YsTs5ltWtEhnq"),
        Source:               models.ToPointer("http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/"),
        SourcePostUrl:        models.ToPointer("http://cheezburger.com/5282328320"),
        SourceTld:            models.ToPointer("cheezburger.com"),
        TrendingDatetime:     models.ToPointer(parseTime(time.RFC3339, "2013-08-01 12:41:48", func(err error) { log.Fatalln(err) })),
        Type:                 models.ToPointer(models.TypeEnum_GIF),
        UpdateDatetime:       models.ToPointer(parseTime(time.RFC3339, "2013-08-01 12:41:48", func(err error) { log.Fatalln(err) })),
        Url:                  models.ToPointer("http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq"),
        Username:             models.ToPointer("JoeCool4000"),
    }

}
```



