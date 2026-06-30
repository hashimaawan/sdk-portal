# Get Vault Items

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkl0ZW1zJTJGR2V0VmF1bHRJdGVtcw

```ruby
def get_vault_items(vault_uuid,
                    filter: nil)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `String` | Template, Required | The UUID of the Vault to fetch Items from<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `filter` | `String` | Query, Optional | Filter the Item collection based on Item name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`Array[Item]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/item.md).


# Example Usage

```ruby
vault_uuid = 'vaultUuid2'

filter = 'title eq "Some Item Name"'

result = items_api.get_vault_items(
  vault_uuid,
  filter: filter
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
| 404 | Vault not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |



