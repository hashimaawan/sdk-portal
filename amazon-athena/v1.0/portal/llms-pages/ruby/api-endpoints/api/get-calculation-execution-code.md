# Get Calculation Execution Code

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZQ

Retrieves the unencrypted code that was executed for the calculation.

```ruby
def get_calculation_execution_code(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-16.md) | Header, Required | - |
| `body` | [`GetCalculationExecutionCodeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/get-calculation-execution-code-request.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`GetCalculationExecutionCodeResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/get-calculation-execution-code-response.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget16::ENUM_AMAZONATHENAGETCALCULATIONEXECUTIONCODE

body = GetCalculationExecutionCodeRequest.new(
  calculation_execution_id: 'CalculationExecutionId8'
)

result = client_api.get_calculation_execution_code(
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



