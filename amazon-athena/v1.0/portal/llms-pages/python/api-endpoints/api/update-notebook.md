# Update Notebook

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZU5vdGVib29r

Updates the contents of a Spark notebook.

```python
def update_notebook(self,
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
| `x_amz_target` | [`XAmzTarget56Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-56.md) | Header, Required | - |
| `body` | [`UpdateNotebookInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/update-notebook-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

`Any`


# Example Usage

```python
x_amz_target = XAmzTarget56Enum.ENUM_AMAZONATHENAUPDATENOTEBOOK

body = UpdateNotebookInput(
    notebook_id='NotebookId6',
    payload='Payload2',
    mtype=NotebookType2Enum.IPYNB
)

result = client_controller.update_notebook(
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
| 482 | TooManyRequestsException | `APIException` |



