# Update Vault Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkl0ZW1zJTJGVXBkYXRlVmF1bHRJdGVt

```python
def update_vault_item(self,
                     vault_uuid,
                     item_uuid,
                     body=None)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `str` | Template, Required | The UUID of the Item's Vault<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `item_uuid` | `str` | Template, Required | The UUID of the Item to update<br><br>**Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `body` | [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/full-item.md) | Body, Optional | - |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FullItem`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/full-item.md).


# Example Usage

```python
vault_uuid = 'vaultUuid2'

item_uuid = 'itemUuid6'

body = FullItem(
    category=Category.MEMBERSHIP,
    vault=Vault1(
        id='id6'
    ),
    favorite=False,
    urls=[
        Url(
            href='https://example.com',
            primary=True
        ),
        Url(
            href='https://example.org'
        )
    ]
)

result = items_api.update_vault_item(
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
| 400 | Unable to create item due to invalid input | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 401 | Invalid or missing token | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 403 | Unauthorized access | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |



