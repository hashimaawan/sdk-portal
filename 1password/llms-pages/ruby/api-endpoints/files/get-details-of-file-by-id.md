# Get Details of File by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0RGV0YWlsc09mRmlsZUJ5SWQ

```ruby
def get_details_of_file_by_id(vault_uuid,
                              item_uuid,
                              file_uuid,
                              inline_files: nil)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `UUID \| String` | Template, Required | The UUID of the Vault to fetch Item from |
| `item_uuid` | `UUID \| String` | Template, Required | The UUID of the Item to fetch File from |
| `file_uuid` | `UUID \| String` | Template, Required | The UUID of the File to fetch |
| `inline_files` | `TrueClass \| FalseClass` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`File`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/file.md).


# Example Usage

```ruby
vault_uuid = '00002186-0000-0000-0000-000000000000'

item_uuid = '0000141a-0000-0000-0000-000000000000'

file_uuid = '000008e0-0000-0000-0000-000000000000'

inline_files = true

result = files_api.get_details_of_file_by_id(
  vault_uuid,
  item_uuid,
  file_uuid,
  inline_files: inline_files
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
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |



