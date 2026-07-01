# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type Any.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `frames` | `str` | Optional | The number of frames in this GIF. |
| `height` | `str` | Optional | The height of this GIF in pixels. |
| `mp_4` | `str` | Optional | The URL for this GIF in .MP4 format. |
| `mp_4_size` | `str` | Optional | The size in bytes of the .MP4 file corresponding to this GIF. |
| `size` | `str` | Optional | The size of this GIF in bytes. |
| `url` | `str` | Optional | The publicly-accessible direct URL for this GIF. |
| `webp` | `str` | Optional | The URL for this GIF in .webp format. |
| `webp_size` | `str` | Optional | The size in bytes of the .webp file corresponding to this GIF. |
| `width` | `str` | Optional | The width of this GIF in pixels. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from giphyapi.models.image import Image

image = Image(
    frames='15',
    height='200',
    mp_4='https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.mp4',
    mp_4_size='25123',
    size='32381',
    url='https://media1.giphy.com/media/cZ7rmKfFYOvYI/200.gif',
    webp='https://media1.giphy.com/media/cZ7rmKfFYOvYI/giphy.webp',
    webp_size='12321',
    width='320',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



