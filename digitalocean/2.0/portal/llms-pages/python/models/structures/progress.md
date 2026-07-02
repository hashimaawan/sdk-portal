# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [Any](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md).*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_steps` | `int` | Optional | - |
| `pending_steps` | `int` | Optional | - |
| `running_steps` | `int` | Optional | - |
| `steps` | [`List[AStepThatIsRunAsPartOfTheDeploymentSLifecycle]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `success_steps` | `int` | Optional | - |
| `summary_steps` | [`List[AStepThatIsRunAsPartOfTheDeploymentSLifecycle]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `total_steps` | `int` | Optional | - |
| `additional_properties` | [`Dict[str, Any]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from digitaloceanapi.models.a_step_that_is_run_as_part_of_the_deployment_s_lifecycle import AStepThatIsRunAsPartOfTheDeploymentSLifecycle
from digitaloceanapi.models.progress import Progress
from digitaloceanapi.models.reason import Reason

progress = Progress(
    error_steps=3,
    pending_steps=2,
    running_steps=2,
    steps=[
        AStepThatIsRunAsPartOfTheDeploymentSLifecycle(
            component_name='component_name0',
            ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            message_base='message_base4',
            name='name2',
            reason=Reason(
                code='code2',
                message='message4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AStepThatIsRunAsPartOfTheDeploymentSLifecycle(
            component_name='component_name0',
            ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            message_base='message_base4',
            name='name2',
            reason=Reason(
                code='code2',
                message='message4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        ),
        AStepThatIsRunAsPartOfTheDeploymentSLifecycle(
            component_name='component_name0',
            ended_at=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            message_base='message_base4',
            name='name2',
            reason=Reason(
                code='code2',
                message='message4',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    success_steps=4,
    total_steps=5,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



