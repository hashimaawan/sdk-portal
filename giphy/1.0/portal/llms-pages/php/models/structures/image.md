# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type array.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `frames` | `?string` | Optional | The number of frames in this GIF. | getFrames(): ?string | setFrames(?string frames): void |
| `height` | `?string` | Optional | The height of this GIF in pixels. | getHeight(): ?string | setHeight(?string height): void |
| `mp4` | `?string` | Optional | The URL for this GIF in .MP4 format. | getMp4(): ?string | setMp4(?string mp4): void |
| `mp4Size` | `?string` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. | getMp4Size(): ?string | setMp4Size(?string mp4Size): void |
| `size` | `?string` | Optional | The size of this GIF in bytes. | getSize(): ?string | setSize(?string size): void |
| `url` | `?string` | Optional | The publicly-accessible direct URL for this GIF. | getUrl(): ?string | setUrl(?string url): void |
| `webp` | `?string` | Optional | The URL for this GIF in .webp format. | getWebp(): ?string | setWebp(?string webp): void |
| `webpSize` | `?string` | Optional | The size in bytes of the .webp file corresponding to this GIF. | getWebpSize(): ?string | setWebpSize(?string webpSize): void |
| `width` | `?string` | Optional | The width of this GIF in pixels. | getWidth(): ?string | setWidth(?string width): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use GiphyApiLib\Models\Builders\ImageBuilder;
use GiphyApiLib\ApiHelper;

$image = ImageBuilder::init()
    ->frames('15')
    ->height('200')
    ->mp4('https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4')
    ->mp4Size('25123')
    ->size('32381')
    ->url('https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif')
    ->webp('https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp')
    ->webpSize('12321')
    ->width('320')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



