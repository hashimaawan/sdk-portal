# A Step that Is Run as Part of the Deployment S Lifecycle

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkElMjUyMHN0ZXAlMjUyMHRoYXQlMjUyMGlzJTI1MjBydW4lMjUyMGFzJTI1MjBwYXJ0JTI1MjBvZiUyNTIwdGhlJTI1MjBkZXBsb3ltZW50JTI1MjdzJTI1MjBsaWZlY3ljbGU

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`AStepThatIsRunAsPartOfTheDeploymentSLifecycle`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `component_name` | `str` | Optional | - |
| `ended_at` | `datetime` | Optional | - |
| `message_base` | `str` | Optional | The base of a human-readable description of the step intended to be combined with the component name for presentation. For example:<br><br>`message_base` = "Building service"<br>`component_name` = "api" |
| `name` | `str` | Optional | - |
| `reason` | [`Reason`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/reason.md) | Optional | - |
| `started_at` | `datetime` | Optional | - |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/enumerations/status-2.md) | Optional | **Default**: `"UNKNOWN"` |
| `steps` | [`List[Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.a_step_that_is_run_as_part_of_the_deployment_s_lifecycle import AStepThatIsRunAsPartOfTheDeploymentSLifecycle
from digitaloceanapi.models.reason import Reason
from digitaloceanapi.models.status_2 import Status2

a_step_that_is_run_as_part_of_the_deployment_s_lifecycle = AStepThatIsRunAsPartOfTheDeploymentSLifecycle(
    component_name='component',
    ended_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    message_base='Building service',
    name='example_step',
    reason=Reason(
        code='code2',
        message='message4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    started_at=dateutil.parser.parse('2020-11-19T20:27:18Z'),
    status=Status2.SUCCESS,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



