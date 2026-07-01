# Delete an SSH Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNTSCUyNTIwS2V5cyUyRkRlbGV0ZSUyNTIwYW4lMjUyMFNTSCUyNTIwa2V5

Deletes an SSH key. It cannot be used anymore.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_an_ssh_key(self,
                     id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | ID of the SSH key |


# Response Type

**204**: SSH key deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 'id0'

result = ssh_keys_api.delete_an_ssh_key(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



