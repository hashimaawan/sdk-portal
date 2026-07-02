# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reused_previous_result` | `bool` | Required | - |


# Example

```python
from amazonathena.models.result_reuse_information import ResultReuseInformation

result_reuse_information = ResultReuseInformation(
    reused_previous_result=False
)
```



