# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXR1czE

*This model accepts additional fields of type Any.*


# Class Name

`Status1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `submission_date_time` | `datetime` | Optional | - |
| `completion_date_time` | `datetime` | Optional | - |
| `state` | [`CalculationExecutionState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `state_change_reason` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.calculation_execution_state_1 import CalculationExecutionState1
from amazonathena.models.status_1 import Status1

status_1 = Status1(
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=CalculationExecutionState1.COMPLETED,
    state_change_reason='StateChangeReason4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



