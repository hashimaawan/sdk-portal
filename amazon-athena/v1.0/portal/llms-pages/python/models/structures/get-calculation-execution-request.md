# Get Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVxdWVzdA


# Class Name

`GetCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |


# Example

```python
from amazonathena.models.get_calculation_execution_request import GetCalculationExecutionRequest

get_calculation_execution_request = GetCalculationExecutionRequest(
    calculation_execution_id='CalculationExecutionId0'
)
```



