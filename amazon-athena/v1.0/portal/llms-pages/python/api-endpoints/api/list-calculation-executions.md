# List Calculation Executions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnM

Lists the calculations that have been submitted to a session in descending order. Newer calculations are listed first; older calculations are listed later.

```python
def list_calculation_executions(self,
                               x_amz_target,
                               body,
                               x_amz_content_sha_256=None,
                               x_amz_date=None,
                               x_amz_algorithm=None,
                               x_amz_credential=None,
                               x_amz_security_token=None,
                               x_amz_signature=None,
                               x_amz_signed_headers=None,
                               max_results=None,
                               next_token=None)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget32Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-32.md) | Header, Required | - |
| `body` | [`ListCalculationExecutionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-calculation-executions-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |
| `max_results` | `str` | Query, Optional | Pagination limit |
| `next_token` | `str` | Query, Optional | Pagination token |


# Response Type

**200**: Success

[`ListCalculationExecutionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-calculation-executions-response.md)


# Example Usage

```python
x_amz_target = XAmzTarget32Enum.ENUM_AMAZONATHENALISTCALCULATIONEXECUTIONS

body = ListCalculationExecutionsRequest(
    session_id='SessionId2'
)

result = client_controller.list_calculation_executions(
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



