# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/java/x-redirect/JTI0bSUyRkltYWdl


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Frames` | `String` | Optional | The number of frames in this GIF. | String getFrames() | setFrames(String frames) |
| `Height` | `String` | Optional | The height of this GIF in pixels. | String getHeight() | setHeight(String height) |
| `Mp4` | `String` | Optional | The URL for this GIF in .MP4 format. | String getMp4() | setMp4(String mp4) |
| `Mp4Size` | `String` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. | String getMp4Size() | setMp4Size(String mp4Size) |
| `Size` | `String` | Optional | The size of this GIF in bytes. | String getSize() | setSize(String size) |
| `Url` | `String` | Optional | The publicly-accessible direct URL for this GIF. | String getUrl() | setUrl(String url) |
| `Webp` | `String` | Optional | The URL for this GIF in .webp format. | String getWebp() | setWebp(String webp) |
| `WebpSize` | `String` | Optional | The size in bytes of the .webp file corresponding to this GIF. | String getWebpSize() | setWebpSize(String webpSize) |
| `Width` | `String` | Optional | The width of this GIF in pixels. | String getWidth() | setWidth(String width) |


# Example

```java
import com.giphy.api.models.Image;

Image image = new Image.Builder()
    .frames("15")
    .height("200")
    .mp4("https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4")
    .mp4Size("25123")
    .size("32381")
    .url("https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif")
    .webp("https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp")
    .webpSize("12321")
    .width("320")
    .build();
```



