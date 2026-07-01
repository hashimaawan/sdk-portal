# Attach Volume to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRkF0dGFjaCUyNTIwVm9sdW1lJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Attaches a Volume to a Server. Works only if the Server is in the same Location as the Volume.

:information_source: **Note** This endpoint does not require authentication.

```csharp
AttachVolumeToAServerAsync(
    int id,
    Models.AttachVolumeRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `body` | [`AttachVolumeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/attach-volume-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `attach_volume` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ActionResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md).


# Example Usage

```csharp
int id = 112;
AttachVolumeRequest body = new AttachVolumeRequest
{
    Server = 43,
    Automount = false,
};

try
{
    ApiResponse<ActionResponse> result = await volumeActionsApi.AttachVolumeToAServerAsync(
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
    "command": "attach_volume",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 43,
        "type": "server"
      },
      {
        "id": 554,
        "type": "volume"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



