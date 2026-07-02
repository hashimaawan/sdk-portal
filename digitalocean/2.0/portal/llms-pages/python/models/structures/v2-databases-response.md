# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databases` | [`List[Database1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/database-1.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.database_1 import Database1
from digitaloceanapi.models.engine_1 import Engine1
from digitaloceanapi.models.maintenance_window import MaintenanceWindow
from digitaloceanapi.models.v_2_databases_response import V2DatabasesResponse

v_2_databases_response = V2DatabasesResponse(
    databases=[
        Database1(
            engine=Engine1.REDIS,
            name='name6',
            num_nodes=242,
            region='region2',
            size='size4',
            connection=Connection(
                database='database2',
                host='host0',
                password='password2',
                port=174,
                ssl=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            db_names=[
                'db_names7',
                'db_names8'
            ],
            id='0000031c-0000-0000-0000-000000000000',
            maintenance_window=MaintenanceWindow(
                day='day0',
                hour='hour8',
                description=[
                    'description3',
                    'description2'
                ],
                pending=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        Database1(
            engine=Engine1.REDIS,
            name='name6',
            num_nodes=242,
            region='region2',
            size='size4',
            connection=Connection(
                database='database2',
                host='host0',
                password='password2',
                port=174,
                ssl=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            created_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            db_names=[
                'db_names7',
                'db_names8'
            ],
            id='0000031c-0000-0000-0000-000000000000',
            maintenance_window=MaintenanceWindow(
                day='day0',
                hour='hour8',
                description=[
                    'description3',
                    'description2'
                ],
                pending=False,
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



