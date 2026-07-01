# Detach a Load Balancer from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGRGV0YWNoJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwZnJvbSUyNTIwYSUyNTIwTmV0d29yaw

Detaches a Load Balancer from a network.

:information_source: **Note** This endpoint does not require authentication.

```go
DetachALoadBalancerFromANetwork(
    ctx context.Context,
    id int,
    body *models.LoadBalancersActionsDetachFromNetworkRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`*models.LoadBalancersActionsDetachFromNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancers-actions-detach-from-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `detach_from_network` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.LoadBalancersActionsDetachFromNetworkRequest{
    Network:               float64(4711),
}

apiResponse, err := loadBalancerActionsApi.DetachALoadBalancerFromANetwork(ctx, id, &body)
if err != nil {
    log.Fatalln(err)
} else {
    // Printing the result and response
    fmt.Println(apiResponse.Data)
    fmt.Println(apiResponse.Response.StatusCode)
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



