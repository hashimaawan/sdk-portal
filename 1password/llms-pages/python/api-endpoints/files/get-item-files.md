# Get Item Files

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRkZpbGVzJTJGR2V0SXRlbUZpbGVz

```python
def get_item_files(self,
                  vault_uuid,
                  item_uuid,
                  inline_files=None)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `vault_uuid` | `uuid\|str` | Template, Required | The UUID of the Vault to fetch Items from |
| `item_uuid` | `uuid\|str` | Template, Required | The UUID of the Item to fetch files from |
| `inline_files` | `bool` | Query, Optional | Tells server to return the base64-encoded file contents in the response. |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`List[File]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/file.md).


# Example Usage

```python
vault_uuid = '00002186-0000-0000-0000-000000000000'

item_uuid = '0000141a-0000-0000-0000-000000000000'

inline_files = True

result = files_api.get_item_files(
    vault_uuid,
    item_uuid,
    inline_files=inline_files
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
| 404 | Item not found | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |
| 413 | File content too large to display | [`ErrorResponseException`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/exceptions/error-response.md) |



