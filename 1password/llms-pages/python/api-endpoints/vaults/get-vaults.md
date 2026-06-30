# Get Vaults

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/python/x-redirect/JTI0ZSUyRlZhdWx0cyUyRkdldFZhdWx0cw

```python
def get_vaults(self,
              filter=None)
```


# Authentication

This endpoint requires [ConnectToken](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/getting-started/quickstart/authorization.md)


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `filter` | `str` | Query, Optional | Filter the Vault collection based on Vault name using SCIM eq filter |


# Response Type

**200**: OK

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`List[Vault]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/python/models/structures/vault.md).


# Example Usage

```python
filter = 'name eq "Some Vault Name"'

result = vaults_api.get_vaults(
    filter=filter
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



