# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdl


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Frames` | `*string` | Optional | The number of frames in this GIF. |
| `Height` | `*string` | Optional | The height of this GIF in pixels. |
| `Mp4` | `*string` | Optional | The URL for this GIF in .MP4 format. |
| `Mp4Size` | `*string` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. |
| `Size` | `*string` | Optional | The size of this GIF in bytes. |
| `Url` | `*string` | Optional | The publicly-accessible direct URL for this GIF. |
| `Webp` | `*string` | Optional | The URL for this GIF in .webp format. |
| `WebpSize` | `*string` | Optional | The size in bytes of the .webp file corresponding to this GIF. |
| `Width` | `*string` | Optional | The width of this GIF in pixels. |


# Example

```go
package main

import (
    "giphyapi/models"
)

func main() {
    image := models.Image{
        Frames:               models.ToPointer("15"),
        Height:               models.ToPointer("200"),
        Mp4:                  models.ToPointer("https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4"),
        Mp4Size:              models.ToPointer("25123"),
        Size:                 models.ToPointer("32381"),
        Url:                  models.ToPointer("https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif"),
        Webp:                 models.ToPointer("https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp"),
        WebpSize:             models.ToPointer("12321"),
        Width:                models.ToPointer("320"),
    }

}
```



