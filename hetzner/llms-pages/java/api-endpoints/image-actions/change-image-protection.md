# Change Image Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBJbWFnZSUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of the Image. Can only be used on snapshots.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> changeImageProtectionAsync(
    final int id,
    final ImagesActionsChangeProtectionRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |
| `body` | [`ImagesActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/images-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
ImagesActionsChangeProtectionRequest body = new ImagesActionsChangeProtectionRequest.Builder()
    .delete(true)
    .build();

imageActionsController.changeImageProtectionAsync(id, body).thenAccept(result -> {
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
        "type": "image"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



