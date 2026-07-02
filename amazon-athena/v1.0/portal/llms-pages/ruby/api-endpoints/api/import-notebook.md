# Import Notebook

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0ZSUyRiUyRkltcG9ydE5vdGVib29r

Imports a single <code>ipynb</code> file to a Spark enabled workgroup. The maximum file size that can be imported is 10 megabytes. If an <code>ipynb</code> file with the same name already exists in the workgroup, throws an error.

```ruby
def import_notebook(x_amz_target,
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
| `x_amz_target` | [`XAmzTarget30`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/x-amz-target-30.md) | Header, Required | - |
| `body` | [`ImportNotebookInput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/import-notebook-input.md) | Body, Required | - |
| `x_amz_content_sha_256` | `String` | Header, Optional | - |
| `x_amz_date` | `String` | Header, Optional | - |
| `x_amz_algorithm` | `String` | Header, Optional | - |
| `x_amz_credential` | `String` | Header, Optional | - |
| `x_amz_security_token` | `String` | Header, Optional | - |
| `x_amz_signature` | `String` | Header, Optional | - |
| `x_amz_signed_headers` | `String` | Header, Optional | - |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ImportNotebookOutput`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/import-notebook-output.md).


# Example Usage

```ruby
x_amz_target = XAmzTarget30::ENUM_AMAZONATHENAIMPORTNOTEBOOK

body = ImportNotebookInput.new(
  work_group: 'WorkGroup8',
  name: 'Name6',
  payload: 'Payload2',
  type: NotebookType2::IPYNB
)

result = client_api.import_notebook(
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



