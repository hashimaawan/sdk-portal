# Create Notebook

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZU5vdGVib29r

Creates an empty <code>ipynb</code> file in the specified Apache Spark enabled workgroup. Throws an error if a file in the workgroup with the same name already exists.

```python
def create_notebook(self,
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
| `x_amz_target` | [`XAmzTarget5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-5.md) | Header, Required | - |
| `body` | [`CreateNotebookInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/create-notebook-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`CreateNotebookOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/create-notebook-output.md).


# Example Usage

```python
x_amz_target = XAmzTarget5.ENUM_AMAZONATHENACREATENOTEBOOK

body = CreateNotebookInput(
    work_group='WorkGroup8',
    name='Name6'
)

result = client_api.create_notebook(
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
| 482 | TooManyRequestsException | `ApiException` |



