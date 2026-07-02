# Start Calculation Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlN0YXJ0Q2FsY3VsYXRpb25FeGVjdXRpb24

Submits calculations for execution within a session. You can supply the code to run as an inline code block within the request.

```ruby
def start_calculation_execution(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget46Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-46.md) | Header, Required | - |
| `body` | [`StartCalculationExecutionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-calculation-execution-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

[`StartCalculationExecutionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-calculation-execution-response.md)


# Example Usage

```ruby
x_amz_target = XAmzTarget46Enum::ENUM_AMAZONATHENASTARTCALCULATIONEXECUTION

body = StartCalculationExecutionRequest.new(
  'SessionId2',
  nil,
  GetCalculationExecutionCodeResponse.new
)

result = client_controller.start_calculation_execution(
  x_amz_target,
  body
)
puts result
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 480 | InternalServerException | `APIException` |
| 481 | InvalidRequestException | `APIException` |
| 482 | ResourceNotFoundException | `APIException` |



