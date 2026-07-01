# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `downsized` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getDownsized(): ?Image | setDownsized(?Image downsized): void |
| `downsizedLarge` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getDownsizedLarge(): ?Image | setDownsizedLarge(?Image downsizedLarge): void |
| `downsizedMedium` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getDownsizedMedium(): ?Image | setDownsizedMedium(?Image downsizedMedium): void |
| `downsizedSmall` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getDownsizedSmall(): ?Image | setDownsizedSmall(?Image downsizedSmall): void |
| `downsizedStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getDownsizedStill(): ?Image | setDownsizedStill(?Image downsizedStill): void |
| `fixedHeight` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedHeight(): ?Image | setFixedHeight(?Image fixedHeight): void |
| `fixedHeightDownsampled` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedHeightDownsampled(): ?Image | setFixedHeightDownsampled(?Image fixedHeightDownsampled): void |
| `fixedHeightSmall` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedHeightSmall(): ?Image | setFixedHeightSmall(?Image fixedHeightSmall): void |
| `fixedHeightSmallStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedHeightSmallStill(): ?Image | setFixedHeightSmallStill(?Image fixedHeightSmallStill): void |
| `fixedHeightStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedHeightStill(): ?Image | setFixedHeightStill(?Image fixedHeightStill): void |
| `fixedWidth` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedWidth(): ?Image | setFixedWidth(?Image fixedWidth): void |
| `fixedWidthDownsampled` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedWidthDownsampled(): ?Image | setFixedWidthDownsampled(?Image fixedWidthDownsampled): void |
| `fixedWidthSmall` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedWidthSmall(): ?Image | setFixedWidthSmall(?Image fixedWidthSmall): void |
| `fixedWidthSmallStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedWidthSmallStill(): ?Image | setFixedWidthSmallStill(?Image fixedWidthSmallStill): void |
| `fixedWidthStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getFixedWidthStill(): ?Image | setFixedWidthStill(?Image fixedWidthStill): void |
| `looping` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getLooping(): ?Image | setLooping(?Image looping): void |
| `original` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getOriginal(): ?Image | setOriginal(?Image original): void |
| `originalStill` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getOriginalStill(): ?Image | setOriginalStill(?Image originalStill): void |
| `preview` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getPreview(): ?Image | setPreview(?Image preview): void |
| `previewGif` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getPreviewGif(): ?Image | setPreviewGif(?Image previewGif): void |


# Example

```php
use GiphyAPILib\Models\Builders\ImagesBuilder;
use GiphyAPILib\Models\Builders\ImageBuilder;

$images = ImagesBuilder::init()
    ->downsized(
        ImageBuilder::init()
            ->frames('frames0')
            ->height('height8')
            ->mp4('mp40')
            ->mp4Size('mp4_size2')
            ->size('size2')
            ->build()
    )
    ->downsizedLarge(
        ImageBuilder::init()
            ->frames('frames6')
            ->height('height4')
            ->mp4('mp46')
            ->mp4Size('mp4_size8')
            ->size('size8')
            ->build()
    )
    ->downsizedMedium(
        ImageBuilder::init()
            ->frames('frames2')
            ->height('height0')
            ->mp4('mp42')
            ->mp4Size('mp4_size4')
            ->size('size4')
            ->build()
    )
    ->downsizedSmall(
        ImageBuilder::init()
            ->frames('frames0')
            ->height('height8')
            ->mp4('mp40')
            ->mp4Size('mp4_size2')
            ->size('size2')
            ->build()
    )
    ->downsizedStill(
        ImageBuilder::init()
            ->frames('frames4')
            ->height('height4')
            ->mp4('mp46')
            ->mp4Size('mp4_size8')
            ->size('size2')
            ->build()
    )
    ->build();
```



