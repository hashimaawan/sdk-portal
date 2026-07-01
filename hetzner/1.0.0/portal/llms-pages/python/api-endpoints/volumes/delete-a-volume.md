# Delete a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlZvbHVtZXMlMkZEZWxldGUlMjUyMGElMjUyMFZvbHVtZQ

Deletes a volume. All Volume data is irreversibly destroyed. The Volume must not be attached to a Server and it must not have delete protection enabled.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_volume(self,
                   id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `str` | Template, Required | ID of the Volume |


# Response Type

**204**: Volume deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 'id0'

result = volumes_api.delete_a_volume(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



