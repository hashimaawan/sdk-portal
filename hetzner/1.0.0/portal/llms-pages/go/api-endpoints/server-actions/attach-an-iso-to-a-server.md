# Attach an ISO to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwYW4lMjUyMElTTyUyNTIwdG8lMjUyMGElMjUyMFNlcnZlcg

Attaches an ISO to a Server. The Server will immediately see it as a new disk. An already attached ISO will automatically be detached before the new ISO is attached.

Servers with attached ISOs have a modified boot order: They will try to boot from the ISO first before falling back to hard disk.

:information_source: **Note** This endpoint does not require authentication.

```go
AttachAnIsoToAServer(
    ctx context.Context,
    id int,
    body *models.ServersActionsAttachIsoRequest) (
    models.ApiResponse[models.ActionResponse],
    error)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`*models.ServersActionsAttachIsoRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/servers-actions-attach-iso-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action-response.md).


# Example Usage

```go
ctx := context.Background()

id := 112

body := models.ServersActionsAttachIsoRequest{
    Iso:                   "FreeBSD-11.0-RELEASE-amd64-dvd1",
}

apiResponse, err := serverActionsApi.AttachAnIsoToAServer(ctx, id, &body)
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
    "command": "attach_iso",
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



