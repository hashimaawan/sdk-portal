# Resize Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRlJlc2l6ZSUyNTIwVm9sdW1l

Changes the size of a Volume. Note that downsizing a Volume is not possible.

:information_source: **Note** This endpoint does not require authentication.

```csharp
ResizeVolumeAsync(
    int id,
    Models.VolumesActionsResizeRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `body` | [`VolumesActionsResizeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/volumes-actions-resize-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `resize_volume` Action

[`Task<Models.ActionResponse>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/action-response.md)


# Example Usage

```csharp
int id = 112;
VolumesActionsResizeRequest body = new VolumesActionsResizeRequest
{
    Size = 50,
};

try
{
    ActionResponse result = await volumeActionsController.ResizeVolumeAsync(
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
    "command": "resize_volume",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
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



