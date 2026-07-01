# Add a Route to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZBZGQlMjUyMGElMjUyMHJvdXRlJTI1MjB0byUyNTIwYSUyNTIwTmV0d29yaw

Adds a route entry to a Network.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def add_a_route_to_a_network(id,
                             body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Network |
| `body` | [`AddDeleteRouteRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/add-delete-route-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_route` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md).


# Example Usage

```ruby
id = 112

body = AddDeleteRouteRequest.new(
  destination: '10.100.1.0/24',
  gateway: '10.0.1.1'
)

result = network_actions_api.add_a_route_to_a_network(
  id,
  body: body
)

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
    "command": "add_route",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



