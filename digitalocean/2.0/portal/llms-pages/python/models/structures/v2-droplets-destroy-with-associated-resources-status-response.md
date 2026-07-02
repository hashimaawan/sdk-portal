# V2 Droplets Destroy with Associated Resources Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTdGF0dXMlMjUyMFJlc3BvbnNl

An objects containing information about a resources scheduled for deletion.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completed_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format indicating when the requested action was completed. |
| `droplet` | [`Droplet1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/droplet-1.md) | Optional | An object containing information about a resource scheduled for deletion. |
| `failures` | `int` | Optional | A count of the associated resources that failed to be destroyed, if any. |
| `resources` | [`Resources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/resources.md) | Optional | An object containing additional information about resource related to a Droplet requested to be destroyed. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.droplet_1 import Droplet1
from digitaloceanapi.models.resources import Resources
from digitaloceanapi.models.v_2_droplets_destroy_with_associated_resources_status_response import V2DropletsDestroyWithAssociatedResourcesStatusResponse

v_2_droplets_destroy_with_associated_resources_status_response = V2DropletsDestroyWithAssociatedResourcesStatusResponse(
    completed_at=dateutil.parser.parse('2020-04-01T18:11:49Z'),
    droplet=Droplet1(
        destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        error_message='error_message2',
        id='id0',
        name='name0',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    failures=0,
    resources=Resources(
        floating_ips=[
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        reserved_ips=[
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message2',
                id='id0',
                name='name0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message2',
                id='id0',
                name='name0',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        snapshots=[
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message4',
                id='id2',
                name='name2',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        volume_snapshots=[
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message0',
                id='id8',
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message0',
                id='id8',
                name='name8',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            )
        ],
        volumes=[
            Droplet1(
                destroyed_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
                error_message='error_message8',
                id='id6',
                name='name6',
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



