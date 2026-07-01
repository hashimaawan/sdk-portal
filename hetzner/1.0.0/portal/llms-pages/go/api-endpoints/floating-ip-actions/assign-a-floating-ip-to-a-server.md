# Assign a Floating IP to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkFzc2lnbiUyNTIwYSUyNTIwRmxvYXRpbmclMjUyMElQJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Assigns a Floating IP to a Server.

:information_source: **Note** This endpoint does not require authentication.

```go
AssignAFloatingIpToAServer(
    ctx context.Context,
    id int,
    body *models.AssignFloatingIpRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`*models.AssignFloatingIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/assign-floating-ip-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `assign` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.AssignFloatingIpRequest{
    Server:                42,
}

apiResponse, err := floatingIpActionsApi.AssignAFloatingIpToAServer(ctx, id, &body)
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
    "command": "assign_floating_ip",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      },
      {
        "id": 4711,
        "type": "floating_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



