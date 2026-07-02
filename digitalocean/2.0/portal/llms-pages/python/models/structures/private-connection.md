# Private Connection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlByaXZhdGVDb25uZWN0aW9u

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`PrivateConnection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | `str` | Optional, Read-only | The name of the default database. |
| `host` | `str` | Optional, Read-only | The FQDN pointing to the database cluster's current primary node. |
| `password` | `str` | Optional, Read-only | The randomly generated password for the default user. |
| `port` | `int` | Optional, Read-only | The port on which the database cluster is listening. |
| `ssl` | `bool` | Optional, Read-only | A boolean value indicating if the connection should be made over SSL. |
| `uri` | `str` | Optional, Read-only | A connection string in the format accepted by the `psql` command. This is provided as a convenience and should be able to be constructed by the other attributes. |
| `user` | `str` | Optional, Read-only | The default user for the database. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.private_connection import PrivateConnection

private_connection = PrivateConnection(
    database='defaultdb',
    host='backend-do-user-19081923-0.db.ondigitalocean.com',
    password='wv78n3zpz42xezdk',
    port=25060,
    ssl=True,
    uri='postgres://doadmin:wv78n3zpz42xezdk@backend-do-user-19081923-0.db.ondigitalocean.com:25060/defaultdb?sslmode=require',
    user='doadmin',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



