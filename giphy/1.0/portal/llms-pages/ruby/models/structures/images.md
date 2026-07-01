# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.

*This model accepts additional fields of type Object.*


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `downsized` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_large` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_medium` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `downsized_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_height_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `fixed_width_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `looping` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `original` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `original_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `preview` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `preview_gif` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
images = Images.new(
  downsized: Image.new(
    frames: 'frames0',
    height: 'height8',
    mp4: 'mp40',
    mp4_size: 'mp4_size2',
    size: 'size2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  downsized_large: Image.new(
    frames: 'frames6',
    height: 'height4',
    mp4: 'mp46',
    mp4_size: 'mp4_size8',
    size: 'size8',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  downsized_medium: Image.new(
    frames: 'frames2',
    height: 'height0',
    mp4: 'mp42',
    mp4_size: 'mp4_size4',
    size: 'size4',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  downsized_small: Image.new(
    frames: 'frames0',
    height: 'height8',
    mp4: 'mp40',
    mp4_size: 'mp4_size2',
    size: 'size2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  downsized_still: Image.new(
    frames: 'frames4',
    height: 'height4',
    mp4: 'mp46',
    mp4_size: 'mp4_size8',
    size: 'size2',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



