# Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlBvb2w

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Pool`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/connection.md) | Optional | - |
| `db` | `str` | Required | The database for use with the connection pool. |
| `mode` | `str` | Required | The PGBouncer transaction mode for the connection pool. The allowed values are session, transaction, and statement. |
| `name` | `str` | Required | A unique name for the connection pool. Must be between 3 and 60 characters. |
| `private_connection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/private-connection.md) | Optional | - |
| `size` | `int` | Required | The desired size of the PGBouncer connection pool. The maximum allowed size is determined by the size of the cluster's primary node. 25 backend server connections are allowed for every 1GB of RAM. Three are reserved for maintenance. For example, a primary node with 1 GB of RAM allows for a maximum of 22 backend server connections while one with 4 GB would allow for 97. Note that these are shared across all connection pools in a cluster. |
| `user` | `str` | Optional | The name of the user for use with the connection pool. When excluded, all sessions connect to the database as the inbound user. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.pool import Pool
from digitaloceanapi.models.private_connection import PrivateConnection

pool = Pool(
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
)
```



