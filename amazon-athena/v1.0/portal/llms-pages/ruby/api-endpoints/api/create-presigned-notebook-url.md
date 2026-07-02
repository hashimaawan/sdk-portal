# Create Presigned Notebook Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZVByZXNpZ25lZE5vdGVib29rVXJs

Gets an authentication token and the URL at which the notebook can be accessed. During programmatic access, <code>CreatePresignedNotebookUrl</code> must be called every 10 minutes to refresh the authentication token. For information about granting programmatic access, see <a href="https://docs.aws.amazon.com/athena/latest/ug/setting-up.html#setting-up-grant-programmatic-access">Grant programmatic access</a>.

```ruby
def create_presigned_notebook_url(x_amz_target,
                                  body,
                                  x_amz_content_sha256: nil,
                                  x_amz_date: nil,
                                  x_amz_algorithm: nil,
                                  x_amz_credential: nil,
                                  x_amz_security_token: nil,
                                  x_amz_signature: nil,
                                  x_amz_signed_headers: nil)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-7.md) | Header, Required | - |
| `body` | [`CreatePresignedNotebookUrlRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/create-presigned-notebook-url-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`CreatePresignedNotebookUrlResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/create-presigned-notebook-url-response.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget7::ENUM_AMAZONATHENACREATEPRESIGNEDNOTEBOOKURL

body = CreatePresignedNotebookUrlRequest.new(
  session_id: 'SessionId2'
)

result = client_api.create_presigned_notebook_url(
  x_amz_target,
  body
)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `APIException` |
| 481 | InvalidRequestException | `APIException` |
| 482 | ResourceNotFoundException | `APIException` |



