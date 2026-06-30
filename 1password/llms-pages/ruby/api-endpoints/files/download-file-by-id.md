# Download File by ID

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkZpbGVzJTJGRG93bmxvYWRGaWxlQnlJRA

```ruby
def download_file_by_id(vault_uuid,
                        item_uuid,
                        file_uuid)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `UUID \| String` | Template, Required | The UUID of the Vault the item is in |
| `item_uuid` | `UUID \| String` | Template, Required | The UUID of the Item the File is in |
| `file_uuid` | `String` | Template, Required | UUID of the file to get content from |


# Response Type

**200**: Success

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type `Binary`.


# Example Usage

```ruby
vault_uuid = '00002186-0000-0000-0000-000000000000'

item_uuid = '0000141a-0000-0000-0000-000000000000'

file_uuid = 'fileUuid2'

result = files_api.download_file_by_id(
  vault_uuid,
  item_uuid,
  file_uuid
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
| 404 | File not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |



