# Delete a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZEZWxldGUlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Deletes a Floating IP. If it is currently assigned to a Server it will automatically get unassigned.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_floating_ip(self,
                        id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**204**: Floating IP deleted

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance.


# Example Usage

```python
id = 112

result = floating_i_ps_api.delete_a_floating_ip(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



