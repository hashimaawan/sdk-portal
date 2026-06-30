# Update Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRkl0ZW1zJTJGVXBkYXRlVmF1bHRJdGVt

```ruby
def update_vault_item(vault_uuid,
                      item_uuid,
                      body: nil)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `String` | Template, Required | The UUID of the Item's Vault<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `item_uuid` | `String` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/full-item.md) | Body, Optional | - |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/full-item.md).


# Example Usage

```ruby
vault_uuid = 'vaultUuid2'

item_uuid = 'itemUuid6'

body = FullItem.new(
  category: Category::MEMBERSHIP,
  vault: Vault1.new(
    id: 'id6'
  ),
  favorite: false,
  urls: [
    Url.new(
      href: 'https://example.com',
      primary: true
    ),
    Url.new(
      href: 'https://example.org'
    )
  ]
)

result = items_api.update_vault_item(
  vault_uuid,
  item_uuid,
  body: body
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
| 400 | Unable to create item due to invalid input | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/exceptions/error-response.md) |



