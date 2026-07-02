# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `next_token` | `str` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `executors_summary` | [`List[ExecutorsSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/executors-summary.md) | Optional | - |


# Example

```python
from amazonathena.models.executor_state_3_enum import ExecutorState3Enum
from amazonathena.models.executor_type_2_enum import ExecutorType2Enum
from amazonathena.models.executors_summary import ExecutorsSummary
from amazonathena.models.list_executors_response import ListExecutorsResponse

list_executors_response = ListExecutorsResponse(
    session_id='SessionId2',
    next_token='NextToken6',
    executors_summary=[
        ExecutorsSummary(
            executor_id='ExecutorId8',
            executor_type=ExecutorType2Enum.GATEWAY,
            start_date_time=128,
            termination_date_time=236,
            executor_state=ExecutorState3Enum.TERMINATED,
            executor_size=42
        )
    ]
)
```



