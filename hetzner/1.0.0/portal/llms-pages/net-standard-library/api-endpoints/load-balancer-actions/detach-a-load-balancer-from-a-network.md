# Detach a Load Balancer from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGRGV0YWNoJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwZnJvbSUyNTIwYSUyNTIwTmV0d29yaw

Detaches a Load Balancer from a network.

:information_source: **Note** This endpoint does not require authentication.

```csharp
DetachALoadBalancerFromANetworkAsync(
    int id,
    Models.LoadBalancersActionsDetachFromNetworkRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancersActionsDetachFromNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/load-balancers-actions-detach-from-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `detach_from_network` Action

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
LoadBalancersActionsDetachFromNetworkRequest body = new LoadBalancersActionsDetachFromNetworkRequest
{
    Network = 4711,
};

try
{
    ActionResponse result = await loadBalancerActionsController.DetachALoadBalancerFromANetworkAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "detach_from_network",
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



