# Rule 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJ1bGUx

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Rule1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cluster_uuid` | `str` | Optional | A unique ID for the database cluster to which the rule is applied.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall rule was created. |
| `mtype` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/type-7.md) | Required | The type of resource that the firewall rule allows to access the database cluster. |
| `uuid` | `str` | Optional | A unique ID for the firewall rule itself.<br><br>**Constraints**: *Pattern*: `^$\|[0-9a-f]{8}\b-[0-9a-f]{4}-[0-9a-f]{4}-[0-9a-f]{4}-\b[0-9a-f]{12}` |
| `value` | `str` | Required | The ID of the specific resource, the name of a tag applied to a group of resources, or the IP address that the firewall rule allows to access the database cluster. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.rule_1 import Rule1
from digitaloceanapi.models.type_7 import Type7

rule_1 = Rule1(
    mtype=Type7.DROPLET,
    value='ff2a6c52-5a44-4b63-b99c-0e98e7a63d61',
    cluster_uuid='9cc10173-e9ea-4176-9dbc-a4cee4c4ff30',
    created_at=dateutil.parser.parse('2019-01-11T18:37:36Z'),
    uuid='79f26d28-ea8a-41f2-8ad8-8cfcdd020095',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



