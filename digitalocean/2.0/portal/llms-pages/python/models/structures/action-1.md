# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Action1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `str` | Optional | A URL that can be used to access the action. |
| `id` | `int` | Optional | A unique numeric ID that can be used to identify and reference an action. |
| `rel` | `str` | Optional | A string specifying the type of the related action. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.action_1 import Action1

action_1 = Action1(
    href='https://api.digitalocean.com/v2/actions/7515',
    id=7515,
    rel='create',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



