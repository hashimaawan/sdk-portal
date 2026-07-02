# Start Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlN0YXJ0U2Vzc2lvbg

Creates a session for running calculations within a workgroup. The session is ready when it reaches an <code>IDLE</code> state.

```ruby
def start_session(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget48`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-48.md) | Header, Required | - |
| `body` | [`StartSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-session-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`StartSessionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-session-response.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget48::ENUM_AMAZONATHENASTARTSESSION

body = StartSessionRequest.new(
  work_group: 'WorkGroup8',
  engine_configuration: EngineConfiguration1.new(
    max_concurrent_dpus: 94
  )
)

result = client_api.start_session(
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
| 483 | SessionAlreadyExistsException | `APIException` |
| 484 | TooManyRequestsException | `APIException` |



