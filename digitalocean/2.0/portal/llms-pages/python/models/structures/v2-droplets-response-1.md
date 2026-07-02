# V2 Droplets Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/droplet.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.distribution import Distribution
from digitaloceanapi.models.droplet import Droplet
from digitaloceanapi.models.image_1 import Image1
from digitaloceanapi.models.kernel import Kernel
from digitaloceanapi.models.networks import Networks
from digitaloceanapi.models.next_backup_window import NextBackupWindow
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.size import Size
from digitaloceanapi.models.status_8 import Status8
from digitaloceanapi.models.type_10 import Type10
from digitaloceanapi.models.type_11 import Type11
from digitaloceanapi.models.v_2_droplets_response_1 import V2DropletsResponse1
from digitaloceanapi.models.v_4 import V4
from digitaloceanapi.models.v_6 import V6

v_2_droplets_response_1 = V2DropletsResponse1(
    droplet=Droplet(
        backup_ids=[
            156,
            157,
            158
        ],
        created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        disk=150,
        features=[
            'features1'
        ],
        id=28,
        image=Image1(
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            description='description6',
            distribution=Distribution.COREOS,
            error_message='error_message8',
            id=128,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        locked=False,
        memory=64,
        name='name0',
        networks=Networks(
            v_4=[
                V4(
                    gateway='gateway2',
                    ip_address='ip_address2',
                    netmask='netmask2',
                    mtype=Type10.PUBLIC,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                V4(
                    gateway='gateway2',
                    ip_address='ip_address2',
                    netmask='netmask2',
                    mtype=Type10.PUBLIC,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                V4(
                    gateway='gateway2',
                    ip_address='ip_address2',
                    netmask='netmask2',
                    mtype=Type10.PUBLIC,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            v_6=[
                V6(
                    gateway='gateway4',
                    ip_address='ip_address4',
                    netmask=106,
                    mtype=Type11.PUBLIC,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                ),
                V6(
                    gateway='gateway4',
                    ip_address='ip_address4',
                    netmask=106,
                    mtype=Type11.PUBLIC,
                    additional_properties={
                        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                    }
                )
            ],
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        next_backup_window=NextBackupWindow(
            end=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            start=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        region=Region(
            available=False,
            features=[
                'features7',
                'features8',
                'features9'
            ],
            name='name6',
            sizes=[
                'sizes6'
            ],
            slug='slug0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        size=Size(
            available=False,
            description='description0',
            disk=252,
            memory=168,
            price_hourly=121.04,
            price_monthly=162.04,
            regions=[
                'regions5'
            ],
            slug='slug6',
            transfer=150.78,
            vcpus=234,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        size_slug='size_slug0',
        snapshot_ids=[
            145,
            146,
            147
        ],
        status=Status8.NEW,
        tags=[
            'tags5',
            'tags6'
        ],
        vcpus=132,
        volume_ids=[
            'volume_ids0'
        ],
        kernel=Kernel(
            id=16,
            name='name4',
            version='version0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        vpc_uuid='vpc_uuid0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



