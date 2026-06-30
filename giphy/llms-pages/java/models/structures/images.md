# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/java/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Downsized` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getDownsized() | setDownsized(Image downsized) |
| `DownsizedLarge` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getDownsizedLarge() | setDownsizedLarge(Image downsizedLarge) |
| `DownsizedMedium` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getDownsizedMedium() | setDownsizedMedium(Image downsizedMedium) |
| `DownsizedSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getDownsizedSmall() | setDownsizedSmall(Image downsizedSmall) |
| `DownsizedStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getDownsizedStill() | setDownsizedStill(Image downsizedStill) |
| `FixedHeight` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedHeight() | setFixedHeight(Image fixedHeight) |
| `FixedHeightDownsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedHeightDownsampled() | setFixedHeightDownsampled(Image fixedHeightDownsampled) |
| `FixedHeightSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedHeightSmall() | setFixedHeightSmall(Image fixedHeightSmall) |
| `FixedHeightSmallStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedHeightSmallStill() | setFixedHeightSmallStill(Image fixedHeightSmallStill) |
| `FixedHeightStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedHeightStill() | setFixedHeightStill(Image fixedHeightStill) |
| `FixedWidth` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedWidth() | setFixedWidth(Image fixedWidth) |
| `FixedWidthDownsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedWidthDownsampled() | setFixedWidthDownsampled(Image fixedWidthDownsampled) |
| `FixedWidthSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedWidthSmall() | setFixedWidthSmall(Image fixedWidthSmall) |
| `FixedWidthSmallStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedWidthSmallStill() | setFixedWidthSmallStill(Image fixedWidthSmallStill) |
| `FixedWidthStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getFixedWidthStill() | setFixedWidthStill(Image fixedWidthStill) |
| `Looping` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getLooping() | setLooping(Image looping) |
| `Original` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getOriginal() | setOriginal(Image original) |
| `OriginalStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getOriginalStill() | setOriginalStill(Image originalStill) |
| `Preview` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getPreview() | setPreview(Image preview) |
| `PreviewGif` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/java/models/structures/image.md) | Optional | - | Image getPreviewGif() | setPreviewGif(Image previewGif) |


# Example

```java
import com.giphy.api.models.Image;
import com.giphy.api.models.Images;

Images images = new Images.Builder()
    .downsized(new Image.Builder()
        .frames("frames0")
        .height("height8")
        .mp4("mp40")
        .mp4Size("mp4_size2")
        .size("size2")
        .build())
    .downsizedLarge(new Image.Builder()
        .frames("frames6")
        .height("height4")
        .mp4("mp46")
        .mp4Size("mp4_size8")
        .size("size8")
        .build())
    .downsizedMedium(new Image.Builder()
        .frames("frames2")
        .height("height0")
        .mp4("mp42")
        .mp4Size("mp4_size4")
        .size("size4")
        .build())
    .downsizedSmall(new Image.Builder()
        .frames("frames0")
        .height("height8")
        .mp4("mp40")
        .mp4Size("mp4_size2")
        .size("size2")
        .build())
    .downsizedStill(new Image.Builder()
        .frames("frames4")
        .height("height4")
        .mp4("mp46")
        .mp4Size("mp4_size8")
        .size("size2")
        .build())
    .build();
```



