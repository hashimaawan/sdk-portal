# Get an Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkFjdGlvbnMlMkZHZXQlMjUyMGFuJTI1MjBBY3Rpb24

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

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

result = actions_api.get_an_action(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```



