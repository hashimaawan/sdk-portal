# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/statistics-1.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.calculation_execution_state_1 import CalculationExecutionState1
from amazonathena.models.get_calculation_execution_status_response import GetCalculationExecutionStatusResponse
from amazonathena.models.statistics_1 import Statistics1
from amazonathena.models.status_1 import Status1

get_calculation_execution_status_response = GetCalculationExecutionStatusResponse(
    status=Status1(
        submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        state=CalculationExecutionState1.CANCELING,
        state_change_reason='StateChangeReason8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    statistics=Statistics1(
        dpu_execution_in_millis=164,
        progress='Progress6',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



