# Get Calculation Execution Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uUmVzcG9uc2U

*This model accepts additional fields of type Any.*


# Class Name

`GetCalculationExecutionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculation_execution_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `session_id` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `working_directory` | `str` | Optional | **Constraints**: *Maximum Length*: `1024`, *Pattern*: `^(https\|s3\|S3)://([^/]+)/?(.*)$` |
| `status` | [`Status1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/statistics-1.md) | Optional | - |
| `result` | [`Result`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/result.md) | Optional | - |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import dateutil.parser
import jsonpickle

from amazonathena.models.calculation_execution_state_1 import CalculationExecutionState1
from amazonathena.models.get_calculation_execution_response import GetCalculationExecutionResponse
from amazonathena.models.status_1 import Status1

get_calculation_execution_response = GetCalculationExecutionResponse(
    calculation_execution_id='CalculationExecutionId2',
    session_id='SessionId6',
    description='Description4',
    working_directory='WorkingDirectory0',
    status=Status1(
        submission_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        completion_date_time=dateutil.parser.parse('2016-03-13T12:52:32.123Z'),
        state=CalculationExecutionState1.CANCELING,
        state_change_reason='StateChangeReason8',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



