# Get Vault Item by Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkl0ZW1zJTJGR2V0VmF1bHRJdGVtQnlJZA

```python
def get_vault_item_by_id(self,
                        vault_uuid,
                        item_uuid)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `str` | Template, Required | The UUID of the Vault to fetch Item from<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `item_uuid` | `str` | Template, Required | The UUID of the Item to fetch<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/full-item.md).


# Example Usage

```python
vault_uuid = 'vaultUuid2'

item_uuid = 'itemUuid6'

result = items_api.get_vault_item_by_id(
    vault_uuid,
    item_uuid
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |



