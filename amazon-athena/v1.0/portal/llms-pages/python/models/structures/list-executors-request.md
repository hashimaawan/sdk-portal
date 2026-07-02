# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `executor_state_filter` | [`ExecutorState1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/executor-state-1.md) | Optional | - |
| `max_results` | `int` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```python
from amazonathena.models.executor_state_1_enum import ExecutorState1Enum
from amazonathena.models.list_executors_request import ListExecutorsRequest

list_executors_request = ListExecutorsRequest(
    session_id='SessionId6',
    executor_state_filter=ExecutorState1Enum.REGISTERED,
    max_results=100,
    next_token='NextToken2'
)
```



