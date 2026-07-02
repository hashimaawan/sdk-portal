# V2 Databases Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pools` | [`List[Pool]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/pool.md) | Optional, Read-only | An array of connection pool objects. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.pool import Pool
from digitaloceanapi.models.private_connection import PrivateConnection
from digitaloceanapi.models.v_2_databases_pools_response import V2DatabasesPoolsResponse

v_2_databases_pools_response = V2DatabasesPoolsResponse(
    pools=[
        Pool(
            db='db2',
            mode='mode0',
            name='name2',
            size=68,
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
            user='user2',
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



