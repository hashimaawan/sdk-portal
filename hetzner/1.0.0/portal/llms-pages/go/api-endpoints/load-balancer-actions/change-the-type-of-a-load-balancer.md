# Change the Type of a Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjB0aGUlMjUyMFR5cGUlMjUyMG9mJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlcg

Changes the type (Max Services, Max Targets and Max Connections) of a Load Balancer.

**Call specific error codes**

| Code                         | Description                                                     |
|------------------------------|-----------------------------------------------------------------|
| `invalid_load_balancer_type` | The Load Balancer type does not fit for the given Load Balancer |

:information_source: **Note** This endpoint does not require authentication.

```go
ChangeTheTypeOfALoadBalancer(
    ctx context.Context,
    id int,
    body *models.ChangeTypeRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`*models.ChangeTypeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/change-type-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_load_balancer_type` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ChangeTypeRequest{
    LoadBalancerType:      "lb21",
}

apiResponse, err := loadBalancerActionsApi.ChangeTheTypeOfALoadBalancer(ctx, id, &body)
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
    "command": "change_load_balancer_type",
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
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



