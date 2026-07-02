# V2 Databases Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pool` | [`Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pool.md) | Required | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.pool import Pool
from digitaloceanapi.models.private_connection import PrivateConnection
from digitaloceanapi.models.v_2_databases_pools_response_1 import V2DatabasesPoolsResponse1

v_2_databases_pools_response_1 = V2DatabasesPoolsResponse1(
    pool=Pool(
        db='defaultdb',
        mode='transaction',
        name='backend-pool',
        size=10,
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
        private_connection=PrivateConnection(
            database='database4',
            host='host4',
            password='password8',
            port=228,
            ssl=False,
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        user='doadmin',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



