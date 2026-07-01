# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type object.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Frames` | `string` | Optional | The number of frames in this GIF. |
| `Height` | `string` | Optional | The height of this GIF in pixels. |
| `Mp4` | `string` | Optional | The URL for this GIF in .MP4 format. |
| `Mp4Size` | `string` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. |
| `Size` | `string` | Optional | The size of this GIF in bytes. |
| `Url` | `string` | Optional | The publicly-accessible direct URL for this GIF. |
| `Webp` | `string` | Optional | The URL for this GIF in .webp format. |
| `WebpSize` | `string` | Optional | The size in bytes of the .webp file corresponding to this GIF. |
| `Width` | `string` | Optional | The width of this GIF in pixels. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using GiphyApi.Standard.Models;
using GiphyApi.Standard.Utilities;

Image image = new Image
{
    Frames = "15",
    Height = "200",
    Mp4 = "https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4",
    Mp4Size = "25123",
    Size = "32381",
    Url = "https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif",
    Webp = "https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp",
    WebpSize = "12321",
    Width = "320",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



