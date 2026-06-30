# Change Image Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0ZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBJbWFnZSUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of the Image. Can only be used on snapshots.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def change_image_protection(id,
                            body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Image |
| `body` | [`ImagesActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/images-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

body = ImagesActionsChangeProtectionRequest.new(
  true
)

result = image_actions_controller.change_image_protection(
  id,
  body: body
)
puts result
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
        "type": "image"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



