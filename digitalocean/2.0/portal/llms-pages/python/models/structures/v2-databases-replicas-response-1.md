# V2 Databases Replicas Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`V2DatabasesReplicasResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `replica` | [`Replica`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/replica.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.private_connection import PrivateConnection
from digitaloceanapi.models.replica import Replica
from digitaloceanapi.models.v_2_databases_replicas_response_1 import V2DatabasesReplicasResponse1

v_2_databases_replicas_response_1 = V2DatabasesReplicasResponse1(
    replica=Replica(
        name='name6',
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
        id='000007e0-0000-0000-0000-000000000000',
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
        private_network_uuid='private_network_uuid6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



