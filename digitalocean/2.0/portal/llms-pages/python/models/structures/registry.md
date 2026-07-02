# Registry

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlJlZ2lzdHJ5

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Registry`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `datetime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the registry was created. |
| `name` | `str` | Optional | A globally unique name for the container registry. Must be lowercase and be composed only of numbers, letters and `-`, up to a limit of 63 characters.<br><br>**Constraints**: *Maximum Length*: `63`, *Pattern*: `^[a-z0-9-]{1,63}$` |
| `region` | `str` | Optional | Slug of the region where registry data is stored |
| `storage_usage_bytes` | `int` | Optional, Read-only | The amount of storage used in the registry in bytes. |
| `storage_usage_bytes_updated_at` | `datetime` | Optional, Read-only | The time at which the storage usage was updated. Storage usage is calculated asynchronously, and may not immediately reflect pushes to the registry. |
| `subscription` | [`Subscription`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/subscription.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.registry import Registry

registry = Registry(
    created_at=dateutil.parser.parse('2020-03-21T16:02:37Z'),
    name='example',
    region='fra1',
    storage_usage_bytes=29393920,
    storage_usage_bytes_updated_at=dateutil.parser.parse('2020-11-04T21:39:49.530562231Z'),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



