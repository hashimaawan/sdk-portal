# Remove Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGUmVtb3ZlJTI1MjBUYXJnZXQ

Removes a target from a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```python
def remove_target(self,
                 id,
                 body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`RemoveTargetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/remove-target-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `remove_target` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

result = load_balancer_actions_controller.remove_target(id)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "remove_target",
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



