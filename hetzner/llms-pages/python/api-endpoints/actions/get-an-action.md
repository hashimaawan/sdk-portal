# Get an Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFuJTI1MjBBY3Rpb24

Returns a specific Action object.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_action(self,
                 id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Resource |


# Response Type

**200**: The `action` key in the reply has this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

result = actions_controller.get_an_action(id)
print(result)
```



