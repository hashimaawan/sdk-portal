# Replica

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlcGxpY2E

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Replica`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/connection.md) | Optional | - |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a database replica. |
| `name` | `str` | Required | The name to give the read-only replicating |
| `private_connection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/private-connection.md) | Optional | - |
| `private_network_uuid` | `str` | Optional | A string specifying the UUID of the VPC to which the read-only replica will be assigned. If excluded, the replica will be assigned to your account's default VPC for the region. |
| `region` | `str` | Optional | A slug identifier for the region where the read-only replica will be located. If excluded, the replica will be placed in the same region as the cluster. |
| `size` | `str` | Optional | A slug identifier representing the size of the node for the read-only replica. The size of the replica must be at least as large as the node size for the database cluster from which it is replicating. |
| `status` | [`Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `tags` | `List[str]` | Optional | A flat array of tag names as strings to apply to the read-only replica after it is created. Tag names can either be existing or new tags. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.private_connection import PrivateConnection
from digitaloceanapi.models.replica import Replica
from digitaloceanapi.models.status_4 import Status4

replica = Replica(
    name='read-nyc3-01',
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
    created_at=dateutil.parser.parse('2019-01-11T18:37:36Z'),
    id='9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
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
    private_network_uuid='9423cbad-9211-442f-820b-ef6915e99b5f',
    region='nyc3',
    size='db-s-2vcpu-4gb',
    status=Status4.CREATING,
    tags=[
        'production'
    ],
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



