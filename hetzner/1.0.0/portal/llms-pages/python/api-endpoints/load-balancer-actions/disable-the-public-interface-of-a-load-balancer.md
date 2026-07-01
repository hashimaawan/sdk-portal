# Disable the Public Interface of a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGRGlzYWJsZSUyNTIwdGhlJTI1MjBwdWJsaWMlMjUyMGludGVyZmFjZSUyNTIwb2YlMjUyMGElMjUyMExvYWQlMjUyMEJhbGFuY2Vy

Disable the public interface of a Load Balancer. The Load Balancer will be not accessible from the internet via its public IPs.

#### Call specific error codes

| Code                                      | Description                                                                    |
|-------------------------------------------|--------------------------------------------------------------------------------|
| `load_balancer_not_attached_to_network`   |  The Load Balancer is not attached to a network                                |
| `targets_without_use_private_ip`          | The Load Balancer has targets that use the public IP instead of the private IP |

:information_source: **Note** This endpoint does not require authentication.

```python
def disable_the_public_interface_of_a_load_balancer(self,
                                                   id)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |


# Response Type

**201**: The `action` key contains the `disable_public_interface` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/sdk-infrastructure/utilities/apiresponse.md) instance. The `body` property of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md).


# Example Usage

```python
id = 112

result = load_balancer_actions_api.disable_the_public_interface_of_a_load_balancer(id)

if result.is_success():
    print(result.body)
elif result.is_error():
    print(result.errors)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "disable_public_interface",
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



