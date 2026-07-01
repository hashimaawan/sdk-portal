# Images

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlcw

An object containing data for various available formats and sizes of this GIF.


# Class Name

`Images`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `downsized` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `downsized_large` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `downsized_medium` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `downsized_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `downsized_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_height` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_height_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_height_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_height_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_height_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_width` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_width_downsampled` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_width_small` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_width_small_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `fixed_width_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `looping` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `original` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `original_still` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `preview` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `preview_gif` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |


# Example

```python
from giphyapi.models.image import Image
from giphyapi.models.images import Images

images = Images(
    downsized=Image(
        frames='frames0',
        height='height8',
        mp_4='mp40',
        mp_4_size='mp4_size2',
        size='size2'
    ),
    downsized_large=Image(
        frames='frames6',
        height='height4',
        mp_4='mp46',
        mp_4_size='mp4_size8',
        size='size8'
    ),
    downsized_medium=Image(
        frames='frames2',
        height='height0',
        mp_4='mp42',
        mp_4_size='mp4_size4',
        size='size4'
    ),
    downsized_small=Image(
        frames='frames0',
        height='height8',
        mp_4='mp40',
        mp_4_size='mp4_size2',
        size='size2'
    ),
    downsized_still=Image(
        frames='frames4',
        height='height4',
        mp_4='mp46',
        mp_4_size='mp4_size8',
        size='size2'
    )
)
```



