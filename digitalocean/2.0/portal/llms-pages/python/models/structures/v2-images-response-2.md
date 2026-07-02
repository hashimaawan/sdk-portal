# V2 Images Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBJbWFnZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2ImagesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/image-1.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.distribution import Distribution
from digitaloceanapi.models.image_1 import Image1
from digitaloceanapi.models.region_2 import Region2
from digitaloceanapi.models.status_7 import Status7
from digitaloceanapi.models.type_9 import Type9
from digitaloceanapi.models.v_2_images_response_2 import V2ImagesResponse2

v_2_images_response_2 = V2ImagesResponse2(
    image=Image1(
        created_at=dateutil.parser.parse('2020-05-04T22:23:02Z'),
        description='description6',
        distribution=Distribution.UBUNTU,
        error_message='error_message8',
        id=7555620,
        min_disk_size=20,
        name='Nifty New Snapshot',
        public=True,
        regions=[
            Region2.NYC1,
            Region2.NYC2
        ],
        size_gigabytes=2.34,
        slug='nifty1',
        status=Status7.NEW,
        tags=[
            'base-image',
            'prod'
        ],
        mtype=Type9.SNAPSHOT,
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



