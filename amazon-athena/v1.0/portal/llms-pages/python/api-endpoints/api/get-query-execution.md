# Get Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkdldFF1ZXJ5RXhlY3V0aW9u

Returns information about a single execution of a query if you have access to the workgroup in which the query ran. Each time a query executes, information about the query execution is saved with a unique ID.

```python
def get_query_execution(self,
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
| `x_amz_target` | [`XAmzTarget23`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-23.md) | Header, Required | - |
| `body` | [`GetQueryExecutionInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/get-query-execution-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`GetQueryExecutionOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/get-query-execution-output.md).


# Example Usage

```python
x_amz_target = XAmzTarget23.ENUM_AMAZONATHENAGETQUERYEXECUTION

body = GetQueryExecutionInput(
    query_execution_id='QueryExecutionId0'
)

result = client_api.get_query_execution(
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



