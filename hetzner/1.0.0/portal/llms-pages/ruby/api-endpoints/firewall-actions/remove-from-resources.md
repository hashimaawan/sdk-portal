# Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkZpcmV3YWxsJTI1MjBBY3Rpb25zJTJGUmVtb3ZlJTI1MjBmcm9tJTI1MjBSZXNvdXJjZXM

Removes one Firewall from multiple resources.

Currently only Servers (and their public network interfaces) are supported.

#### Call specific error codes

| Code                                  | Description                                                            |
|---------------------------------------|------------------------------------------------------------------------|
| `firewall_already_removed`            | Firewall was already removed from the resource                         |
| `firewall_resource_not_found`         | The resource the Firewall should be attached to was not found          |
| `firewall_managed_by_label_selector`  | Firewall was applied via label selector and cannot be removed manually |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def remove_from_resources(id,
                          body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Firewall |
| `body` | [`RemoveFromResourcesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/remove-from-resources-request.md) | Body, Optional | - |


# Response Type

**201**: The `actions` key contains multiple `remove_firewall` Actions

[`ActionsResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/actions-response.md)


# Example Usage

```ruby
id = 112

body = RemoveFromResourcesRequest.new(
  [
    FirewallRemoveFromResources.new(
      LabelSelector5.new,
      Server9.new(
        42
      ),
      Type7Enum::SERVER
    )
  ]
)

result = firewall_actions_controller.remove_from_resources(
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
      "command": "remove_firewall",
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



