# Database 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRhdGFiYXNlMQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Database1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `connection` | [`Connection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/connection.md) | Optional | - |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the database cluster was created. |
| `db_names` | `List[str]` | Optional, Read-only | An array of strings containing the names of databases created in the database cluster. |
| `engine` | [`Engine1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/engine-1.md) | Required | A slug representing the database engine used for the cluster. The possible values are: "pg" for PostgreSQL, "mysql" for MySQL, "redis" for Redis, and "mongodb" for MongoDB. |
| `id` | `uuid\|str` | Optional, Read-only | A unique ID that can be used to identify and reference a database cluster. |
| `maintenance_window` | [`MaintenanceWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/maintenance-window.md) | Optional | - |
| `name` | `str` | Required | A unique, human-readable name referring to a database cluster. |
| `num_nodes` | `int` | Required | The number of nodes in the database cluster. |
| `private_connection` | [`PrivateConnection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/private-connection.md) | Optional | - |
| `private_network_uuid` | `str` | Optional | A string specifying the UUID of the VPC to which the database cluster will be assigned. If excluded, the cluster when creating a new database cluster, it will be assigned to your account's default VPC for the region.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `project_id` | `uuid\|str` | Optional | The ID of the project that the database cluster is assigned to. If excluded when creating a new database cluster, it will be assigned to your default project. |
| `region` | `str` | Required | The slug identifier for the region where the database cluster is located. |
| `rules` | [`List[Rule1]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/rule-1.md) | Optional | - |
| `size` | `str` | Required | The slug identifier representing the size of the nodes in the database cluster. |
| `status` | [`Status4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-4.md) | Optional, Read-only | A string representing the current status of the database cluster. |
| `tags` | `List[str]` | Optional | An array of tags that have been applied to the database cluster. |
| `users` | [`List[User]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/user.md) | Optional, Read-only | - |
| `version` | `str` | Optional | A string representing the version of the database engine in use for the cluster. |
| `version_end_of_availability` | `str` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. |
| `version_end_of_life` | `str` | Optional, Read-only | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.connection import Connection
from digitaloceanapi.models.database_1 import Database1
from digitaloceanapi.models.engine_1 import Engine1
from digitaloceanapi.models.maintenance_window import MaintenanceWindow
from digitaloceanapi.models.status_4 import Status4

database_1 = Database1(
    engine=Engine1.PG,
    name='backend',
    num_nodes=2,
    region='nyc3',
    size='db-s-2vcpu-4gb',
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
    db_names=[
        'doadmin'
    ],
    id='9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
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
    private_network_uuid='d455e75d-4858-4eec-8c95-da2f0a5f93a7',
    project_id='9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
    status=Status4.CREATING,
    tags=[
        'production'
    ],
    version='10',
    version_end_of_availability='2023-05-09T00:00:00Z',
    version_end_of_life='2023-11-09T00:00:00Z',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



