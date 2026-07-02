# List Application DPU Sizes

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVz

Returns the supported DPU sizes for the supported application runtimes (for example, <code>Athena notebook version 1</code>).

```ruby
def list_application_dpu_sizes(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget31`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-31.md) | Header, Required | - |
| `body` | [`ListApplicationDpuSizesInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-application-dpu-sizes-input.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ListApplicationDpuSizesOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-application-dpu-sizes-output.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget31::ENUM_AMAZONATHENALISTAPPLICATIONDPUSIZES

body = ListApplicationDpuSizesInput.new

result = client_api.list_application_dpu_sizes(
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
| 482 | TooManyRequestsException | `APIException` |



