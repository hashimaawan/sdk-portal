# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```ruby
def get_vaults(filter: nil)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `String` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`Array[Vault]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/ruby/models/structures/vault.md).


# Example Usage

```ruby
filter = 'name eq "Some Vault Name"'

result = vaults_api.get_vaults(filter: filter)

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



