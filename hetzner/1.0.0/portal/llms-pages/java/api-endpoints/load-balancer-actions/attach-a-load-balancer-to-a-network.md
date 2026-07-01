# Attach a Load Balancer to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQXR0YWNoJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwdG8lMjUyMGElMjUyME5ldHdvcms

Attach a Load Balancer to a Network.

**Call specific error codes**

| Code                             | Description                                                           |
|----------------------------------|-----------------------------------------------------------------------|
| `load_balancer_already_attached` | The Load Balancer is already attached to a network                    |
| `ip_not_available`               | The provided Network IP is not available                              |
| `no_subnet_available`            | No Subnet or IP is available for the Load Balancer within the network |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> attachALoadBalancerToANetworkAsync(
    final int id,
    final LoadBalancersActionsAttachToNetworkRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancersActionsAttachToNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancers-actions-attach-to-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `attach_to_network` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
LoadBalancersActionsAttachToNetworkRequest body = new LoadBalancersActionsAttachToNetworkRequest.Builder(
    4711D
)
.ip("10.0.1.1")
.build();

loadBalancerActionsController.attachALoadBalancerToANetworkAsync(id, body).thenAccept(result -> {
    // TODO success callback handler
    System.out.println(result);
}).exceptionally(exception -> {
    // TODO failure callback handler
    exception.printStackTrace();
    return null;
});
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



