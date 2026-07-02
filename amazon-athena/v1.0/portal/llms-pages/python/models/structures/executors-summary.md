# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type Any.*


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executor_id` | `str` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executor_type` | [`ExecutorType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/executor-type-2.md) | Optional | - |
| `start_date_time` | `int` | Optional | - |
| `termination_date_time` | `int` | Optional | - |
| `executor_state` | [`ExecutorState3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/executor-state-3.md) | Optional | - |
| `executor_size` | `int` | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.executor_state_3 import ExecutorState3
from amazonathena.models.executor_type_2 import ExecutorType2
from amazonathena.models.executors_summary import ExecutorsSummary

executors_summary = ExecutorsSummary(
    executor_id='ExecutorId2',
    executor_type=ExecutorType2.GATEWAY,
    start_date_time=204,
    termination_date_time=160,
    executor_state=ExecutorState3.CREATING,
    executor_size=118,
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



