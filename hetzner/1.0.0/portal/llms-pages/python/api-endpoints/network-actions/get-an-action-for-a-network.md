# Get an Action for a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZHZXQlMjUyMGFuJTI1MjBBY3Rpb24lMjUyMGZvciUyNTIwYSUyNTIwTmV0d29yaw

Returns a specific Action for a Network.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_action_for_a_network(self,
                               id,
                               action_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `action_id` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key contains the Network Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

action_id = 224

result = network_actions_controller.get_an_action_for_a_network(
    id,
    action_id
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "add_subnet",
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
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



