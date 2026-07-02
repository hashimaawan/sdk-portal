# Start Calculation Execution Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0bSUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb25SZXF1ZXN0

*This model accepts additional fields of type Any.*


# Class Name

`StartCalculationExecutionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `session_id` | `str` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `str` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `calculation_configuration` | [`GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/get-calculation-execution-code-response.md) | Optional | - |
| `code_block` | `str` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `client_request_token` | `str` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `additional_properties` | `Dict[str, Any]` | Optional | - |


# Example

```python
import jsonpickle

from amazonathena.models.get_calculation_execution_code_response import GetCalculationExecutionCodeResponse
from amazonathena.models.start_calculation_execution_request import StartCalculationExecutionRequest

start_calculation_execution_request = StartCalculationExecutionRequest(
    session_id='SessionId8',
    description='Description6',
    calculation_configuration=GetCalculationExecutionCodeResponse(
        code_block='CodeBlock4',
        additional_properties={
            'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
        }
    ),
    code_block='CodeBlock2',
    client_request_token='ClientRequestToken4',
    additional_properties={
        'exampleAdditionalProperty': jsonpickle.decode('{"key1":"val1","key2":"val2"}')
    }
)
```



