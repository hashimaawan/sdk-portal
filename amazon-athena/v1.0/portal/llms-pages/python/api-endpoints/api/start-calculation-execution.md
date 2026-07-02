# Start Calculation Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb24

Submits calculations for execution within a session. You can supply the code to run as an inline code block within the request.

```python
def start_calculation_execution(self,
                               x_amz_target,
                               body,
                               x_amz_content_sha_256=None,
                               x_amz_date=None,
                               x_amz_algorithm=None,
                               x_amz_credential=None,
                               x_amz_security_token=None,
                               x_amz_signature=None,
                               x_amz_signed_headers=None)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget46Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-46.md) | Header, Required | - |
| `body` | [`StartCalculationExecutionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/start-calculation-execution-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

[`StartCalculationExecutionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/start-calculation-execution-response.md)


# Example Usage

```python
x_amz_target = XAmzTarget46Enum.ENUM_AMAZONATHENASTARTCALCULATIONEXECUTION

body = StartCalculationExecutionRequest(
    session_id='SessionId2'
)

result = client_controller.start_calculation_execution(
    x_amz_target,
    body
)
print(result)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `APIException` |
| 481 | InvalidRequestException | `APIException` |
| 482 | ResourceNotFoundException | `APIException` |



