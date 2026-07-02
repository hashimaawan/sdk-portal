# List Named Queries

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3ROYW1lZFF1ZXJpZXM

<p>Provides a list of available query IDs only for queries saved in the specified workgroup. Requires that you have access to the specified workgroup. If a workgroup is not specified, lists the saved queries for the primary workgroup.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="http://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


```ruby
def list_named_queries(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget37`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-37.md) | Header, Required | - |
| `body` | [`ListNamedQueriesInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-named-queries-input.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ListNamedQueriesOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-named-queries-output.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget37::ENUM_AMAZONATHENALISTNAMEDQUERIES

body = ListNamedQueriesInput.new

result = client_api.list_named_queries(
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



