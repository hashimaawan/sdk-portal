# Resize Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRlJlc2l6ZSUyNTIwVm9sdW1l

Changes the size of a Volume. Note that downsizing a Volume is not possible.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> resizeVolumeAsync(
    final int id,
    final VolumesActionsResizeRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `body` | [`VolumesActionsResizeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/volumes-actions-resize-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `resize_volume` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
VolumesActionsResizeRequest body = new VolumesActionsResizeRequest.Builder(
    50D
)
.build();

volumeActionsController.resizeVolumeAsync(id, body).thenAccept(result -> {
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



