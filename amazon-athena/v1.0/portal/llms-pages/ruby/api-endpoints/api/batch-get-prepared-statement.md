# Batch Get Prepared Statement

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnQ

Returns the details of a single prepared statement or a list of up to 256 prepared statements for the array of prepared statement names that you provide. Requires you to have access to the workgroup to which the prepared statements belong. If a prepared statement cannot be retrieved for the name specified, the statement is listed in <code>UnprocessedPreparedStatementNames</code>.

```ruby
def batch_get_prepared_statement(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-1.md) | Header, Required | - |
| `body` | [`BatchGetPreparedStatementInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/batch-get-prepared-statement-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

[`BatchGetPreparedStatementOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/batch-get-prepared-statement-output.md)


# Example Usage

```ruby
x_amz_target = XAmzTarget1Enum::ENUM_AMAZONATHENABATCHGETPREPAREDSTATEMENT

body = BatchGetPreparedStatementInput.new(
  [
    'PreparedStatementNames0',
    'PreparedStatementNames1',
    'PreparedStatementNames2'
  ],
  'WorkGroup8'
)

result = client_controller.batch_get_prepared_statement(
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



