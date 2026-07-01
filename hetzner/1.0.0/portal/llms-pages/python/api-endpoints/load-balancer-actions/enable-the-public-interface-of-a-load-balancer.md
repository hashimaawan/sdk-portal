# Enable the Public Interface of a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGRW5hYmxlJTI1MjB0aGUlMjUyMHB1YmxpYyUyNTIwaW50ZXJmYWNlJTI1MjBvZiUyNTIwYSUyNTIwTG9hZCUyNTIwQmFsYW5jZXI

Enable the public interface of a Load Balancer. The Load Balancer will be accessible from the internet via its public IPs.

:information_source: **Note** This endpoint does not require authentication.

```python
def enable_the_public_interface_of_a_load_balancer(self,
                                                  id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**201**: The `action` key contains the `enable_public_interface` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

result = load_balancer_actions_api.enable_the_public_interface_of_a_load_balancer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "enable_public_interface",
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
      },
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



