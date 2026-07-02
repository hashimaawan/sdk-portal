# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0

*This model accepts additional fields of type Any.*


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_groups` | [`List[WorkGroupSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `next_token` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.engine_version_1 import EngineVersion1
from amazonathena.models.list_work_groups_output import ListWorkGroupsOutput
from amazonathena.models.work_group_state_1 import WorkGroupState1
from amazonathena.models.work_group_summary import WorkGroupSummary

list_work_groups_output = ListWorkGroupsOutput(
    work_groups=[
        WorkGroupSummary(
            name='Name4',
            state=WorkGroupState1.ENABLED,
            description='Description0',
            creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
            engine_version=EngineVersion1(
                selected_engine_version='SelectedEngineVersion4',
                effective_engine_version='EffectiveEngineVersion6',
                additional_properties={
                    'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
                }
            ),
            additional_properties={
                'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
            }
        )
    ],
    next_token='NextToken2',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



