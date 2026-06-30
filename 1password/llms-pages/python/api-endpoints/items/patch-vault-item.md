# Patch Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkl0ZW1zJTJGUGF0Y2hWYXVsdEl0ZW0

Applies a modified [RFC6902 JSON Patch](https://tools.ietf.org/html/rfc6902) document to an Item or ItemField. This endpoint only supports `add`, `remove` and `replace` operations.

When modifying a specific ItemField, the ItemField's ID in the `path` attribute of the operation object: `/fields/{fieldId}`

```python
def patch_vault_item(self,
                    vault_uuid,
                    item_uuid,
                    body=None)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `str` | Template, Required | The UUID of the Vault the item is in<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `item_uuid` | `str` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`List[Patch]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/patch.md) | Body, Optional | - |


# Response Type

**200**: OK - Item updated. If no Patch operations were provided, Item is unmodified.

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/full-item.md).


# Example Usage

```python
vault_uuid = 'vaultUuid2'

item_uuid = 'itemUuid6'

body = [
    Patch(
        op=Op.ADD,
        path='/fields',
        value=jsonpickle.decode('{"label":"New Field","type":"string","value":"hunter2"}')
    )
]

result = items_api.patch_vault_item(
    vault_uuid,
    item_uuid,
    body=body
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



