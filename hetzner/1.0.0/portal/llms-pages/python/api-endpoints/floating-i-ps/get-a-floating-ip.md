# Get a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUHMlMkZHZXQlMjUyMGElMjUyMEZsb2F0aW5nJTI1MjBJUA

Returns a specific Floating IP object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_a_floating_ip(self,
                     id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |


# Response Type

**200**: The `floating_ip` key in the reply contains a Floating IP object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`FloatingIpsResponse2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/floating-ips-response-2.md).


# Example Usage

```python
id = 112

result = floating_i_ps_api.get_a_floating_ip(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



