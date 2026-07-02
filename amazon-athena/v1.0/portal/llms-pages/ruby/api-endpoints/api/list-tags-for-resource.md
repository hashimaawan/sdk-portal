# List Tags for Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RUYWdzRm9yUmVzb3VyY2U

Lists the tags associated with an Athena workgroup or data catalog resource.

```ruby
def list_tags_for_resource(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget44Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-44.md) | Header, Required | - |
| `body` | [`ListTagsForResourceInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-tags-for-resource-input.md) | Body, Required | - |
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

[`ListTagsForResourceOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-tags-for-resource-output.md)


# Example Usage

```ruby
x_amz_target = XAmzTarget44Enum::ENUM_AMAZONATHENALISTTAGSFORRESOURCE

body = ListTagsForResourceInput.new(
  'ResourceARN4'
)

result = client_controller.list_tags_for_resource(
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



