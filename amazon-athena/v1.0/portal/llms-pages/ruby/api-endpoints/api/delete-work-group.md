# Delete Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkRlbGV0ZVdvcmtHcm91cA

Deletes the workgroup with the specified name. The primary workgroup cannot be deleted.

```ruby
def delete_work_group(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget13Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-13.md) | Header, Required | - |
| `body` | [`DeleteWorkGroupInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/delete-work-group-input.md) | Body, Required | - |
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
x_amz_target = XAmzTarget13Enum::ENUM_AMAZONATHENADELETEWORKGROUP

body = DeleteWorkGroupInput.new(
  'WorkGroup8'
)

result = client_controller.delete_work_group(
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



