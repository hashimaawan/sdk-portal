# Image Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/python/x-redirect/JTI0bSUyRkltYWdlT2JqZWN0

*This model accepts additional fields of type Any.*


# Class Name

`ImageObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `url` | `str` | Required | The source URL of the image. |
| `height` | `int` | Required | The image height in pixels. |
| `width` | `int` | Required | The image width in pixels. |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from spotifywebapiwithfixesandimprovementsfromsonallux.models.image_object import ImageObject

image_object = ImageObject(
    url='https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
    height=300,
    width=300,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



