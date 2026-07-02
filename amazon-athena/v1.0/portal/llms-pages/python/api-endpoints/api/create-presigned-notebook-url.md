# Create Presigned Notebook Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/python/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJs

Gets an authentication token and the URL at which the notebook can be accessed. During programmatic access, <code>CreatePresignedNotebookUrl</code> must be called every 10 minutes to refresh the authentication token. For information about granting programmatic access, see <a href="https://docs.aws.amazon.com/athena/latest/ug/setting-up.html#setting-up-grant-programmatic-access">Grant programmatic access</a>.

```python
def create_presigned_notebook_url(self,
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
| `x_amz_target` | [`XAmzTarget7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/enumerations/x-amz-target-7.md) | Header, Required | - |
| `body` | [`CreatePresignedNotebookUrlRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/create-presigned-notebook-url-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `str` | Header, Optional | - |
| `x_amz_date` | `str` | Header, Optional | - |
| `x_amz_algorithm` | `str` | Header, Optional | - |
| `x_amz_credential` | `str` | Header, Optional | - |
| `x_amz_security_token` | `str` | Header, Optional | - |
| `x_amz_signature` | `str` | Header, Optional | - |
| `x_amz_signed_headers` | `str` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`CreatePresignedNotebookUrlResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/python/models/structures/create-presigned-notebook-url-response.md).


# Example Usage

```python
x_amz_target = XAmzTarget7.ENUM_AMAZONATHENACREATEPRESIGNEDNOTEBOOKURL

body = CreatePresignedNotebookUrlRequest(
    session_id='SessionId2'
)

result = client_api.create_presigned_notebook_url(
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



