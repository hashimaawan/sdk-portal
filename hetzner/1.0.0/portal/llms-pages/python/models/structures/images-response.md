# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`List[Image]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/image.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/meta.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.images_response import ImagesResponse
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.os_flavor import OsFlavor
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_24 import Status24
from hetznercloudapi.models.type_22 import Type22

images_response = ImagesResponse(
    images=[
        Image(
            bound_to=None,
            created='2016-01-30T23:55:00+00:00',
            created_from=CreatedFrom(
                id=1,
                name='Server',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            deleted=None,
            deprecated='2018-02-28T00:00:00+00:00',
            description='Ubuntu 20.04 Standard 64 bit',
            disk_size=10,
            id=42,
            image_size=2.3,
            labels={
                'key0': 'labels0',
                'key1': 'labels1'
            },
            name='ubuntu-20.04',
            os_flavor=OsFlavor.UBUNTU,
            os_version='20.04',
            protection=Protection(
                delete=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            status=Status24.AVAILABLE,
            mtype=Type22.SNAPSHOT,
            rapid_deploy=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



