# Change Primary IP Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBQcmltYXJ5JTI1MjBJUCUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of a Primary IP.

A Primary IP can only be delete protected if its `auto_delete` property is set to `false`.

:information_source: **Note** This endpoint does not require authentication.

```go
ChangePrimaryIpProtection(
    ctx context.Context,
    id int,
    body *models.ChangeProtectionRequest2) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |
| `body` | [`*models.ChangeProtectionRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/change-protection-request-2.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ChangeProtectionRequest2{
    Delete:                models.ToPointer(true),
}

apiResponse, err := primaryIpActionsApi.ChangePrimaryIpProtection(ctx, id, &body)
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
    "command": "change_protection",
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
        "type": "primary_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



