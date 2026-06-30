# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/ruby/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `downsized` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_large` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_medium` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `looping` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `original` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `original_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `preview` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `preview_gif` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/ruby/models/structures/image.md) | Optional | - |


# Example

```ruby
images = Images.new(
  Image.new(
    'frames0',
    'height8',
    'mp40',
    'mp4_size2',
    'size2'
  ),
  Image.new(
    'frames6',
    'height4',
    'mp46',
    'mp4_size8',
    'size8'
  ),
  Image.new(
    'frames2',
    'height0',
    'mp42',
    'mp4_size4',
    'size4'
  ),
  Image.new(
    'frames0',
    'height8',
    'mp40',
    'mp4_size2',
    'size2'
  ),
  Image.new(
    'frames4',
    'height4',
    'mp46',
    'mp4_size8',
    'size2'
  ),
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new,
  Image.new
)
```



