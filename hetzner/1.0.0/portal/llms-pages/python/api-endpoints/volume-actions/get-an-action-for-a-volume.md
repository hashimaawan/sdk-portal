# Get an Action for a Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYW4lMjUyMEFjdGlvbiUyNTIwZm9yJTI1MjBhJTI1MjBWb2x1bWU

Returns a specific Action for a Volume.

:information_source: **Note** This endpoint does not require authentication.

```python
def get_an_action_for_a_volume(self,
                              id,
                              action_id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `action_id` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key contains the Volume Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

action_id = 224

result = volume_actions_api.get_an_action_for_a_volume(
    id,
    action_id
)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "attach_volume",
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



