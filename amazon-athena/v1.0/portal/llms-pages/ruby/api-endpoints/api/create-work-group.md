# Create Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkNyZWF0ZVdvcmtHcm91cA

Creates a workgroup with the specified name. A workgroup can be an Apache Spark enabled workgroup or an Athena SQL workgroup.

```ruby
def create_work_group(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget8Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-8.md) | Header, Required | - |
| `body` | [`CreateWorkGroupInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/create-work-group-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

`Object`


# Example Usage

```ruby
x_amz_target = XAmzTarget8Enum::ENUM_AMAZONATHENACREATEWORKGROUP

body = CreateWorkGroupInput.new(
  'Name6',
  Configuration.new(
    ResultConfiguration1.new(
      nil,
      EncryptionConfiguration2.new(
        envrr
      ),
      nil,
      AclConfiguration1.new(
        envrr
      )
    ),
    nil,
    nil,
    nil,
    nil,
    EngineVersion1.new,
    nil,
    nil,
    CustomerContentEncryptionConfiguration2.new
  ),
  nil,
  []
)

result = client_controller.create_work_group(
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



