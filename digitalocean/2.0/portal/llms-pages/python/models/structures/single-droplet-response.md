# Single Droplet Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlNpbmdsZSUyNTIwRHJvcGxldCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`SingleDropletResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/droplet.md) | Required | - |
| `links` | [`Links1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links-1.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.action_1 import Action1
from digitaloceanapi.models.distribution import Distribution
from digitaloceanapi.models.droplet import Droplet
from digitaloceanapi.models.image_1 import Image1
from digitaloceanapi.models.kernel import Kernel
from digitaloceanapi.models.links_1 import Links1
from digitaloceanapi.models.networks import Networks
from digitaloceanapi.models.next_backup_window import NextBackupWindow
from digitaloceanapi.models.region import Region
from digitaloceanapi.models.region_2 import Region2
from digitaloceanapi.models.single_droplet_response import SingleDropletResponse
from digitaloceanapi.models.size import Size
from digitaloceanapi.models.status_7 import Status7
from digitaloceanapi.models.status_8 import Status8
from digitaloceanapi.models.type_10 import Type10
from digitaloceanapi.models.type_11 import Type11
from digitaloceanapi.models.type_9 import Type9
from digitaloceanapi.models.v_4 import V4
from digitaloceanapi.models.v_6 import V6

single_droplet_response = SingleDropletResponse(
    droplet=Droplet(
        backup_ids=[
            53893572
        ],
        created_at=dateutil.parser.parse('2020-07-21T18:37:44Z'),
        disk=25,
        features=[
            'backups',
            'private_networking',
            'ipv6'
        ],
        id=3164444,
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
        locked=False,
        memory=1024,
        name='example.com',
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
            end=dateutil.parser.parse('2019-12-04T23:00:00Z'),
            start=dateutil.parser.parse('2019-12-04T00:00:00Z'),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        region=Region(
            available=True,
            features=[
                'private_networking',
                'backups',
                'ipv6',
                'metadata',
                'install_agent',
                'storage',
                'image_transfer'
            ],
            name='New York 3',
            sizes=[
                's-1vcpu-1gb',
                's-1vcpu-2gb',
                's-1vcpu-3gb',
                's-2vcpu-2gb',
                's-3vcpu-1gb',
                's-2vcpu-4gb',
                's-4vcpu-8gb',
                's-6vcpu-16gb',
                's-8vcpu-32gb',
                's-12vcpu-48gb',
                's-16vcpu-64gb',
                's-20vcpu-96gb',
                's-24vcpu-128gb',
                's-32vcpu-192g'
            ],
            slug='nyc3',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        size=Size(
            available=True,
            description='Basic',
            disk=25,
            memory=1024,
            price_hourly=0.00743999984115362,
            price_monthly=5,
            regions=[
                'ams2',
                'ams3',
                'blr1',
                'fra1',
                'lon1',
                'nyc1',
                'nyc2',
                'nyc3',
                'sfo1',
                'sfo2',
                'sfo3',
                'sgp1',
                'tor1'
            ],
            slug='s-1vcpu-1gb',
            transfer=1,
            vcpus=1,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        size_slug='s-1vcpu-1gb',
        snapshot_ids=[
            67512819
        ],
        status=Status8.ACTIVE,
        tags=[
            'web',
            'env:prod'
        ],
        vcpus=1,
        volume_ids=[
            '506f78a4-e098-11e5-ad9f-000f53306ae1'
        ],
        kernel=Kernel(
            id=16,
            name='name4',
            version='version0',
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        vpc_uuid='760e09ef-dc84-11e8-981e-3cfdfeaae000',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    links=Links1(
        actions=[
            Action1(
                href='href0',
                id=154,
                rel='rel4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



