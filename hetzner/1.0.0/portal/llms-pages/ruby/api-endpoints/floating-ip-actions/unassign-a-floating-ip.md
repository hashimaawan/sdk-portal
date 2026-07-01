# Unassign a Floating IP

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRlVuYXNzaWduJTI1MjBhJTI1MjBGbG9hdGluZyUyNTIwSVA

Unassigns a Floating IP, resulting in it being unreachable. You may assign it to a Server again at a later time.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def unassign_a_floating_ip(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Floating IP |


# Response Type

**201**: The `action` key contains the `unassign` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md).


# Example Usage

```ruby
id = 112

result = floating_ip_actions_api.unassign_a_floating_ip(id)

if result.success?
  puts result.data
elsif result.error?
  warn result.errors
end
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "unassign_floating_ip",
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
      },
      {
        "id": 4711,
        "type": "floating_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



