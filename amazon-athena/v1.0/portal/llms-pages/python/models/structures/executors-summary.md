# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Class Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executor_id` | `str` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executor_type` | [`ExecutorType2Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/executor-type-2.md) | Optional | - |
| `start_date_time` | `int` | Optional | - |
| `termination_date_time` | `int` | Optional | - |
| `executor_state` | [`ExecutorState3Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/executor-state-3.md) | Optional | - |
| `executor_size` | `int` | Optional | - |


# Example

```python
from amazonathena.models.executor_state_3_enum import ExecutorState3Enum
from amazonathena.models.executor_type_2_enum import ExecutorType2Enum
from amazonathena.models.executors_summary import ExecutorsSummary

executors_summary = ExecutorsSummary(
    executor_id='ExecutorId2',
    executor_type=ExecutorType2Enum.GATEWAY,
    start_date_time=204,
    termination_date_time=160,
    executor_state=ExecutorState3Enum.CREATING,
    executor_size=118
)
```



