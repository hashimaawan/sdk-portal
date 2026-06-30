# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/image.md) | Optional | - |


# Example

```python
from hetznercloudapi.models.created_from import CreatedFrom
from hetznercloudapi.models.image import Image
from hetznercloudapi.models.images_response_1 import ImagesResponse1
from hetznercloudapi.models.os_flavor_enum import OsFlavorEnum
from hetznercloudapi.models.protection import Protection
from hetznercloudapi.models.status_24_enum import Status24Enum
from hetznercloudapi.models.type_22_enum import Type22Enum

images_response_1 = ImagesResponse1(
    image=Image(
        bound_to=186,
        created='created6',
        created_from=CreatedFrom(
            id=60,
            name='name6'
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
        os_flavor=OsFlavorEnum.DEBIAN,
        os_version='os_version4',
        protection=Protection(
            delete=False
        ),
        status=Status24Enum.UNAVAILABLE,
        mtype=Type22Enum.APP,
        rapid_deploy=False
    )
)
```



