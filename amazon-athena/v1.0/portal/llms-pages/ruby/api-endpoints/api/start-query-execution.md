# Start Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRlN0YXJ0UXVlcnlFeGVjdXRpb24

Runs the SQL query statements contained in the <code>Query</code>. Requires you to have access to the workgroup in which the query ran. Running queries against an external catalog requires <a>GetDataCatalog</a> permission to the catalog. For code samples using the Amazon Web Services SDK for Java, see <a href="http://docs.aws.amazon.com/athena/latest/ug/code-samples.html">Examples and Code Samples</a> in the <i>Amazon Athena User Guide</i>.

```ruby
def start_query_execution(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget47Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-47.md) | Header, Required | - |
| `body` | [`StartQueryExecutionInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-query-execution-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

[`StartQueryExecutionOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/start-query-execution-output.md)


# Example Usage

```ruby
x_amz_target = XAmzTarget47Enum::ENUM_AMAZONATHENASTARTQUERYEXECUTION

body = StartQueryExecutionInput.new(
  'QueryString8',
  nil,
  QueryExecutionContext1.new,
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
  [],
  ResultReuseConfiguration1.new(
    ResultReuseByAgeConfiguration2.new
  )
)

result = client_controller.start_query_execution(
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
| 482 | TooManyRequestsException | `APIException` |



