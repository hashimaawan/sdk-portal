# Delete a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlcnMlMkZEZWxldGUlMjUyMGElMjUyMFNlcnZlcg

Deletes a Server. This immediately removes the Server from your account, and it is no longer accessible.

:information_source: **Note** This endpoint does not require authentication.

```python
def delete_a_server(self,
                   id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |


# Response Type

**200**: The `action` key in the reply contains an Action object with this structure

[`ServersResponse1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/servers-response-1.md)


# Example Usage

```python
id = 112

result = servers_controller.delete_a_server(id)
print(result)
```



