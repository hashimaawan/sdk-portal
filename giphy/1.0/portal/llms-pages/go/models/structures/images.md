# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.

*This model accepts additional fields of type interface{}.*


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Downsized` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `DownsizedLarge` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `DownsizedMedium` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `DownsizedSmall` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `DownsizedStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedHeight` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedHeightDownsampled` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedHeightSmall` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedHeightSmallStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedHeightStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedWidth` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedWidthDownsampled` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedWidthSmall` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedWidthSmallStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `FixedWidthStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `Looping` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `Original` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `OriginalStill` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `Preview` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `PreviewGif` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "giphyApi/models"
)

func main() {
    images := models.Images{
        Downsized:              models.ToPointer(models.Image{
            Frames:                models.ToPointer("frames0"),
            Height:                models.ToPointer("height8"),
            Mp4:                   models.ToPointer("mp40"),
            Mp4Size:               models.ToPointer("mp4_size2"),
            Size:                  models.ToPointer("size2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        DownsizedLarge:         models.ToPointer(models.Image{
            Frames:                models.ToPointer("frames6"),
            Height:                models.ToPointer("height4"),
            Mp4:                   models.ToPointer("mp46"),
            Mp4Size:               models.ToPointer("mp4_size8"),
            Size:                  models.ToPointer("size8"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        DownsizedMedium:        models.ToPointer(models.Image{
            Frames:                models.ToPointer("frames2"),
            Height:                models.ToPointer("height0"),
            Mp4:                   models.ToPointer("mp42"),
            Mp4Size:               models.ToPointer("mp4_size4"),
            Size:                  models.ToPointer("size4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        DownsizedSmall:         models.ToPointer(models.Image{
            Frames:                models.ToPointer("frames0"),
            Height:                models.ToPointer("height8"),
            Mp4:                   models.ToPointer("mp40"),
            Mp4Size:               models.ToPointer("mp4_size2"),
            Size:                  models.ToPointer("size2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        DownsizedStill:         models.ToPointer(models.Image{
            Frames:                models.ToPointer("frames4"),
            Height:                models.ToPointer("height4"),
            Mp4:                   models.ToPointer("mp46"),
            Mp4Size:               models.ToPointer("mp4_size8"),
            Size:                  models.ToPointer("size2"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:   map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



