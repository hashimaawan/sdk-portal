# Terminate Session

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlRlcm1pbmF0ZVNlc3Npb24

Terminates an active session. A <code>TerminateSession</code> call on a session that is already inactive (for example, in a <code>FAILED</code>, <code>TERMINATED</code> or <code>TERMINATING</code> state) succeeds but has no effect. Calculations running in the session when <code>TerminateSession</code> is called are forcefully stopped, but may display as <code>FAILED</code> instead of <code>STOPPED</code>.

```ruby
def terminate_session(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget52`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-52.md) | Header, Required | - |
| `body` | [`TerminateSessionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/terminate-session-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`TerminateSessionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/terminate-session-response.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget52::ENUM_AMAZONATHENATERMINATESESSION

body = TerminateSessionRequest.new(
  session_id: 'SessionId2'
)

result = client_api.terminate_session(
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



