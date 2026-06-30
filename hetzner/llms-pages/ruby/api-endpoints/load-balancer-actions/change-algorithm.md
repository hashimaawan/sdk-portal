# Change Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBBbGdvcml0aG0

Change the algorithm that determines to which target new requests are sent.

:information_source: **Note** This endpoint does not require authentication.

```ruby
def change_algorithm(id,
                     body: nil)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `Integer` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancersActionsChangeAlgorithmRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancers-actions-change-algorithm-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_algorithm` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/action-response.md)


# Example Usage

```ruby
id = 112

result = load_balancer_actions_controller.change_algorithm(id)
puts result
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "change_algorithm",
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



