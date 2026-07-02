# List Work Groups

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RXb3JrR3JvdXBz

Lists available workgroups for the account.

```ruby
def list_work_groups(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget45`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-45.md) | Header, Required | - |
| `body` | [`ListWorkGroupsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-work-groups-input.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ListWorkGroupsOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-work-groups-output.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget45::ENUM_AMAZONATHENALISTWORKGROUPS

body = ListWorkGroupsInput.new

result = client_api.list_work_groups(
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



