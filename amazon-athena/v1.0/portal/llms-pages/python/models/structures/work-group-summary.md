# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.


# Class Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `str` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/work-group-state-1.md) | Optional | - |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creation_time` | `datetime` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/engine-version-1.md) | Optional | - |


# Example

```python
import dateutil.parser

from amazonathena.models.engine_version_1 import EngineVersion1
from amazonathena.models.work_group_state_1_enum import WorkGroupState1Enum
from amazonathena.models.work_group_summary import WorkGroupSummary

work_group_summary = WorkGroupSummary(
    name='Name2',
    state=WorkGroupState1Enum.ENABLED,
    description='Description4',
    creation_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    engine_version=EngineVersion1(
        selected_engine_version='SelectedEngineVersion4',
        effective_engine_version='EffectiveEngineVersion6'
    )
)
```



