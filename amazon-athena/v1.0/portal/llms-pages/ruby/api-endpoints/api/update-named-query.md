# Update Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlVwZGF0ZU5hbWVkUXVlcnk

Updates a <a>NamedQuery</a> object. The database or workgroup cannot be updated.

```ruby
def update_named_query(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget55Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-55.md) | Header, Required | - |
| `body` | [`UpdateNamedQueryInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/update-named-query-input.md) | Body, Required | - |
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
x_amz_target = XAmzTarget55Enum::ENUM_AMAZONATHENAUPDATENAMEDQUERY

body = UpdateNamedQueryInput.new(
  'NamedQueryId6',
  'Name6',
  'QueryString8'
)

result = client_controller.update_named_query(
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



