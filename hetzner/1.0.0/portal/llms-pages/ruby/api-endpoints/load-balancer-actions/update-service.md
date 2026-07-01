# Update Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGVXBkYXRlJTI1MjBTZXJ2aWNl

Updates a Load Balancer Service.

#### Call specific error codes

| Code                       | Description                                             |
|----------------------------|---------------------------------------------------------|
| `source_port_already_used` | The source port you are trying to add is already in use |

:information_source: **Note** This endpoint does not require authentication.

```ruby
def update_service(id,
                   body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancerService`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-service.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `update_service` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/sdk-infrastructure/utilities/apiresponse.md) instance. The `data` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/action-response.md).


# Example Usage

```ruby
id = 112

body = LoadBalancerService.new(
  destination_port: 80,
  health_check: LoadBalancerServiceHealthCheck.new(
    interval: 15,
    port: 4711,
    protocol: Protocol6::HTTP,
    retries: 3,
    timeout: 10
  ),
  listen_port: 443,
  protocol: Protocol7::HTTPS,
  proxyprotocol: false
)

result = load_balancer_actions_api.update_service(
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
    "command": "update_service",
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
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



