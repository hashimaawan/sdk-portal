# Droplet 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkRyb3BsZXQx

An object containing information about a resource scheduled for deletion.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Droplet1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `destroyed_at` | `datetime` | Optional | A time value given in ISO8601 combined date and time format indicating when the resource was destroyed if the request was successful. |
| `error_message` | `str` | Optional | A string indicating that the resource was not successfully destroyed and providing additional information. |
| `id` | `str` | Optional | The unique identifier for the resource scheduled for deletion. |
| `name` | `str` | Optional | The name of the resource scheduled for deletion. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.droplet_1 import Droplet1

droplet_1 = Droplet1(
    destroyed_at=dateutil.parser.parse('2020-04-01T18:11:49Z'),
    error_message='error_message4',
    id='61486916',
    name='ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



