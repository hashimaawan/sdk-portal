# Import Notebook

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkltcG9ydE5vdGVib29r

Imports a single <code>ipynb</code> file to a Spark enabled workgroup. The maximum file size that can be imported is 10 megabytes. If an <code>ipynb</code> file with the same name already exists in the workgroup, throws an error.

```python
def import_notebook(self,
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
| `x_amz_target` | [`XAmzTarget30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-30.md) | Header, Required | - |
| `body` | [`ImportNotebookInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/import-notebook-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ImportNotebookOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/import-notebook-output.md).


# Example Usage

```python
x_amz_target = XAmzTarget30.ENUM_AMAZONATHENAIMPORTNOTEBOOK

body = ImportNotebookInput(
    work_group='WorkGroup8',
    name='Name6',
    payload='Payload2',
    mtype=NotebookType2.IPYNB
)

result = client_api.import_notebook(
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



