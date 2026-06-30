# Get an Action for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYW4lMjUyMEFjdGlvbiUyNTIwZm9yJTI1MjBhJTI1MjBTZXJ2ZXI

Returns a specific Action object for a Server.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_action_for_a_server(self,
                              id,
                              action_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `action_id` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key in the reply has this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

action_id = 224

result = server_actions_controller.get_an_action_for_a_server(
    id,
    action_id
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "start_server",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



