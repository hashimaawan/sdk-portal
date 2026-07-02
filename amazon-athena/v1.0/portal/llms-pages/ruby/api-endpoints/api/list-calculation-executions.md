# List Calculation Executions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnM

Lists the calculations that have been submitted to a session in descending order. Newer calculations are listed first; older calculations are listed later.

```ruby
def list_calculation_executions(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget32Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-32.md) | Header, Required | - |
| `body` | [`ListCalculationExecutionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-calculation-executions-request.md) | Body, Required | - |
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

[`ListCalculationExecutionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-calculation-executions-response.md)


# Example Usage

```ruby
x_amz_target = XAmzTarget32Enum::ENUM_AMAZONATHENALISTCALCULATIONEXECUTIONS

body = ListCalculationExecutionsRequest.new(
  'SessionId2',
  envrr
)

result = client_controller.list_calculation_executions(
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



