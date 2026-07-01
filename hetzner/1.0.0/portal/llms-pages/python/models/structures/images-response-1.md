# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Any.*


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/image.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.images_response_1 import ImagesResponse1
from hetznercloudapi.models.os_flavor import OsFlavor
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_24 import Status24
from hetznercloudapi.models.type_22 import Type22

images_response_1 = ImagesResponse1(
    image=Image(
        bound_to=186,
        created='created6',
        created_from=CreatedFrom(
            id=60,
            name='name6',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        deleted='deleted4',
        deprecated='deprecated8',
        description='description6',
        disk_size=244.18,
        id=128,
        image_size=141.34,
        labels={
            'key0': 'labels4'
        },
        name='name6',
        os_flavor=OsFlavor.DEBIAN,
        os_version='os_version4',
        protection=Protection(
            delete=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        status=Status24.UNAVAILABLE,
        mtype=Type22.APP,
        rapid_deploy=False,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



