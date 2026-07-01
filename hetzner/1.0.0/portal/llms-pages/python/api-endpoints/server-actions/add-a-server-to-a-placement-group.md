# Add a Server to a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkFkZCUyNTIwYSUyNTIwU2VydmVyJTI1MjB0byUyNTIwYSUyNTIwUGxhY2VtZW50JTI1MjBHcm91cA

Adds a Server to a Placement Group.

Server must be powered off for this command to succeed.

#### Call specific error codes

| Code                          | Description                                                          |
|-------------------------------|----------------------------------------------------------------------|
| `server_not_stopped`          | The action requires a stopped server                                 |

:information_source: **Note** This endpoint does not require authentication.

```python
def add_a_server_to_a_placement_group(self,
                                     id,
                                     body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`AddToPlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/add-to-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

body = AddToPlacementGroupRequest(
    placement_group=1
)

result = server_actions_controller.add_a_server_to_a_placement_group(
    id,
    body=body
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "add_to_placement_group",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



