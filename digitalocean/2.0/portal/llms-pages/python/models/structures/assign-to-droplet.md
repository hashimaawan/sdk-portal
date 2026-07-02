# Assign to Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkFzc2lnbiUyNTIwdG8lMjUyMERyb3BsZXQ

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`AssignToDroplet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet_id` | `int` | Required | The ID of the Droplet that the floating IP will be assigned to. |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import jsonpickle

from digitaloceanapi.models.assign_to_droplet import AssignToDroplet

assign_to_droplet = AssignToDroplet(
    droplet_id=2457247,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



