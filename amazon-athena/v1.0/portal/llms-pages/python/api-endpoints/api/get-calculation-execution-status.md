# Get Calculation Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVz

Gets the status of a current calculation.

```python
def get_calculation_execution_status(self,
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
| `x_amz_target` | [`XAmzTarget17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-17.md) | Header, Required | - |
| `body` | [`GetCalculationExecutionStatusRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/get-calculation-execution-status-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`GetCalculationExecutionStatusResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/get-calculation-execution-status-response.md).


# Example Usage

```python
x_amz_target = XAmzTarget17.ENUM_AMAZONATHENAGETCALCULATIONEXECUTIONSTATUS

body = GetCalculationExecutionStatusRequest(
    calculation_execution_id='CalculationExecutionId8'
)

result = client_api.get_calculation_execution_status(
    x_amz_target,
    body
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `ApiException` |
| 481 | InvalidRequestException | `ApiException` |
| 482 | ResourceNotFoundException | `ApiException` |



