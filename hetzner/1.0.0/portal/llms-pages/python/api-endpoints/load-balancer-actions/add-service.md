# Add Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQWRkJTI1MjBTZXJ2aWNl

Adds a service to a Load Balancer.

#### Call specific error codes

| Code                       | Description                                             |
|----------------------------|---------------------------------------------------------|
| `source_port_already_used` | The source port you are trying to add is already in use |

:information_source: **Note** This endpoint does not require authentication.

```python
def add_service(self,
               id,
               body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancerService`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancer-service.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_service` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

body = LoadBalancerService(
    destination_port=80,
    health_check=LoadBalancerServiceHealthCheck(
        interval=15,
        port=4711,
        protocol=Protocol6.HTTP,
        retries=3,
        timeout=10
    ),
    listen_port=443,
    protocol=Protocol7.HTTPS,
    proxyprotocol=False
)

result = load_balancer_actions_api.add_service(
    id,
    body=body
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
    "command": "add_service",
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



