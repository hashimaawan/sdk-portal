# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type Any.*


# Class Name

`CalculationStatus`


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
from amazonathena.models.calculation_status import CalculationStatus

calculation_status = CalculationStatus(
    submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
    state=CalculationExecutionState1.CREATING,
    state_change_reason='StateChangeReason4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



