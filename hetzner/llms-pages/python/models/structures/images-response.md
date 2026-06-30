# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`List[Image]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/image.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/meta.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.images_response import ImagesResponse
from hetznercloudapi.models.meta import Meta
from hetznercloudapi.models.os_flavor_enum import OsFlavorEnum
from hetznercloudapi.models.pagination import Pagination
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_24_enum import Status24Enum
from hetznercloudapi.models.type_22_enum import Type22Enum

images_response = ImagesResponse(
    images=[
        Image(
            bound_to=None,
            created='2016-01-30T23:55:00+00:00',
            created_from=CreatedFrom(
                id=1,
                name='Server'
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
            os_flavor=OsFlavorEnum.UBUNTU,
            os_version='20.04',
            protection=Protection(
                delete=False
            ),
            status=Status24Enum.AVAILABLE,
            mtype=Type22Enum.SNAPSHOT,
            rapid_deploy=False
        )
    ],
    meta=Meta(
        pagination=Pagination(
            last_page=77.7,
            next_page=209.18,
            page=17.58,
            per_page=13.34,
            previous_page=50.02,
            total_entries=206.64
        )
    )
)
```



