# Disable Rescue Mode for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkRpc2FibGUlMjUyMFJlc2N1ZSUyNTIwTW9kZSUyNTIwZm9yJTI1MjBhJTI1MjBTZXJ2ZXI

Disables the Hetzner Rescue System for a Server. This makes a Server start from its disks on next reboot.

Rescue Mode is automatically disabled when you first boot into it or if you do not use it for 60 minutes.

Disabling rescue mode will not reboot your Server — you will have to do this yourself.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def disable_rescue_mode_for_a_server(id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Server |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md).


# Example Usage

```ruby
id = 112

result = server_actions_api.disable_rescue_mode_for_a_server(id)

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
    "command": "disable_rescue",
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



