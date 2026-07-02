# List Sessions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RTZXNzaW9ucw

Lists the sessions in a workgroup that are in an active state like <code>CREATING</code>, <code>CREATED</code>, <code>IDLE</code>, or <code>BUSY</code>. Newer sessions are listed first; older sessions are listed later.

```ruby
def list_sessions(x_amz_target,
                  body,
                  x_amz_content_sha256: nil,
                  x_amz_date: nil,
                  x_amz_algorithm: nil,
                  x_amz_credential: nil,
                  x_amz_security_token: nil,
                  x_amz_signature: nil,
                  x_amz_signed_headers: nil,
                  max_results: nil,
                  next_token: nil)
```


# Authentication

This endpoint requires [hmac](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `x_amz_target` | [`XAmzTarget42`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-42.md) | Header, Required | - |
| `body` | [`ListSessionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-sessions-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |
| `max_results` | `String` | Query, Optional | Pagination limit |
| `next_token` | `String` | Query, Optional | Pagination token |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ListSessionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-sessions-response.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget42::ENUM_AMAZONATHENALISTSESSIONS

body = ListSessionsRequest.new(
  work_group: 'WorkGroup8'
)

result = client_api.list_sessions(
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



