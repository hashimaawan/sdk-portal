# List Query Executions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkxpc3RRdWVyeUV4ZWN1dGlvbnM

<p>Provides a list of available query execution IDs for the queries in the specified workgroup. If a workgroup is not specified, returns a list of query execution IDs for the primary workgroup. Requires you to have access to the workgroup in which the queries ran.</p> <p>For code samples using the Amazon Web Services SDK for Java, see <a href="http://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.</p>


```ruby
def list_query_executions(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget41`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-41.md) | Header, Required | - |
| `body` | [`ListQueryExecutionsInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-query-executions-input.md) | Body, Required | - |
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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ListQueryExecutionsOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/list-query-executions-output.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget41::ENUM_AMAZONATHENALISTQUERYEXECUTIONS

body = ListQueryExecutionsInput.new

result = client_api.list_query_executions(
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



