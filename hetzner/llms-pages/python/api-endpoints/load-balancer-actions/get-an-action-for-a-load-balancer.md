# Get an Action for a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGR2V0JTI1MjBhbiUyNTIwQWN0aW9uJTI1MjBmb3IlMjUyMGElMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Returns a specific Action for a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_action_for_a_load_balancer(self,
                                     id,
                                     action_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `action_id` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key contains the Load Balancer Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

action_id = 224

result = load_balancer_actions_controller.get_an_action_for_a_load_balancer(
    id,
    action_id
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "change_protection",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 4711,
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



