# List Prepared Statements

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHM

Lists the prepared statements in the specified workgroup.

```python
def list_prepared_statements(self,
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
| `x_amz_target` | [`XAmzTarget40Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-40.md) | Header, Required | - |
| `body` | [`ListPreparedStatementsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-prepared-statements-input.md) | Body, Required | - |
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

[`ListPreparedStatementsOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/list-prepared-statements-output.md)


# Example Usage

```python
x_amz_target = XAmzTarget40Enum.ENUM_AMAZONATHENALISTPREPAREDSTATEMENTS

body = ListPreparedStatementsInput(
    work_group='WorkGroup8'
)

result = client_controller.list_prepared_statements(
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



