# Attach a Load Balancer to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/python/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQXR0YWNoJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwdG8lMjUyMGElMjUyME5ldHdvcms

Attach a Load Balancer to a Network.

**Call specific error codes**

| Code                             | Description                                                           |
|----------------------------------|-----------------------------------------------------------------------|
| `load_balancer_already_attached` | The Load Balancer is already attached to a network                    |
| `ip_not_available`               | The provided Network IP is not available                              |
| `no_subnet_available`            | No Subnet or IP is available for the Load Balancer within the network |

:information_source: **Note** This endpoint does not require authentication.

```python
def attach_a_load_balancer_to_a_network(self,
                                       id,
                                       body=None)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancersActionsAttachToNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/load-balancers-actions-attach-to-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `attach_to_network` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/python/models/structures/action-response.md)


# Example Usage

```python
id = 112

body = LoadBalancersActionsAttachToNetworkRequest(
    network=4711,
    ip='10.0.1.1'
)

result = load_balancer_actions_controller.attach_a_load_balancer_to_a_network(
    id,
    body=body
)
print(result)
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "attach_to_network",
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



