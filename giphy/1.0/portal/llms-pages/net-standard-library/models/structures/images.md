# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Downsized` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `DownsizedLarge` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `DownsizedMedium` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `DownsizedSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `DownsizedStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedHeight` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedHeightDownsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedHeightSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedHeightSmallStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedHeightStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedWidth` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedWidthDownsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedWidthSmall` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedWidthSmallStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `FixedWidthStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `Looping` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `Original` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `OriginalStill` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `Preview` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |
| `PreviewGif` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/net-standard-library/models/structures/image.md) | Optional | - |


# Example

```csharp
using GiphyAPI.Standard.Models;

Images images = new Images
{
    Downsized = new Image
    {
        Frames = "frames0",
        Height = "height8",
        Mp4 = "mp40",
        Mp4Size = "mp4_size2",
        Size = "size2",
    },
    DownsizedLarge = new Image
    {
        Frames = "frames6",
        Height = "height4",
        Mp4 = "mp46",
        Mp4Size = "mp4_size8",
        Size = "size8",
    },
    DownsizedMedium = new Image
    {
        Frames = "frames2",
        Height = "height0",
        Mp4 = "mp42",
        Mp4Size = "mp4_size4",
        Size = "size4",
    },
    DownsizedSmall = new Image
    {
        Frames = "frames0",
        Height = "height8",
        Mp4 = "mp40",
        Mp4Size = "mp4_size2",
        Size = "size2",
    },
    DownsizedStill = new Image
    {
        Frames = "frames4",
        Height = "height4",
        Mp4 = "mp46",
        Mp4Size = "mp4_size8",
        Size = "size2",
    },
};
```



