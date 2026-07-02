# Resources 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlc291cmNlczE

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Resources1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assigned_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format that represents when the project was created. |
| `links` | [`Links4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/links-4.md) | Optional | The links object contains the `self` object, which contains the resource relationship. |
| `status` | [`Status14`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-14.md) | Optional | The status of assigning and fetching the resources. |
| `urn` | `str` | Optional | The uniform resource name (URN) for the resource in the format do:resource_type:resource_id.<br><br>**Constraints**: *Pattern*: `^do:(dbaas\|domain\|droplet\|floatingip\|loadbalancer\|space\|volume\|kubernetes\|vpc):.*` |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.links_4 import Links4
from digitaloceanapi.models.resources_1 import Resources1
from digitaloceanapi.models.status_14 import Status14

resources_1 = Resources1(
    assigned_at=dateutil.parser.parse('2018-09-28T19:26:37Z'),
    links=Links4(
        mself='self2',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    status=Status14.OK,
    urn='do:droplet:13457723',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



