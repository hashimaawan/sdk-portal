# Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGQXBwbHklMjUyMHRvJTI1MjBSZXNvdXJjZXM

Applies one Firewall to multiple resources.

Currently servers (public network interface) and label selectors are supported.

#### Call specific error codes

| Code                          | Description                                                   |
|-------------------------------|---------------------------------------------------------------|
| `firewall_already_applied`    | Firewall was already applied on resource                      |
| `incompatible_network_type`   | The Network type is incompatible for the given resource       |
| `firewall_resource_not_found` | The resource the Firewall should be attached to was not found |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def apply_to_resources(id,
                       body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Firewall |
| `body` | [`ApplyToResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/apply-to-resources-request.md) | Body, Optional | - |


# Response Type

**201**: The `actions` key contains multiple `apply_firewall` Actions

[`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/actions-response.md)


# Example Usage

```ruby
id = 112

body = ApplyToResourcesRequest.new(
  [
    FirewallApplyToResources.new(
      LabelSelector5.new,
      Server9.new(
        42
      ),
      Type7Enum::SERVER
    )
  ]
)

result = firewall_actions_controller.apply_to_resources(
  id,
  body: body
)
puts result
```


# Example Response *(as JSON)*

```json
{
  "actions": [
    {
      "command": "apply_firewall",
      "error": {
        "code": "action_failed",
        "message": "Action failed"
      },
      "finished": "2016-01-30T23:56:00+00:00",
      "id": 14,
      "progress": 100,
      "resources": [
        {
          "id": 42,
          "type": "server"
        },
        {
          "id": 38,
          "type": "firewall"
        }
      ],
      "started": "2016-01-30T23:55:00+00:00",
      "status": "success"
    }
  ]
}
```



