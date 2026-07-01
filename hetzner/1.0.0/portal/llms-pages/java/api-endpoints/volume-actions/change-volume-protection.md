# Change Volume Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwVm9sdW1lJTI1MjBQcm90ZWN0aW9u

Changes the protection configuration of a Volume.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionResponse>> changeVolumeProtectionAsync(
    final int id,
    final VolumesActionsChangeProtectionRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `body` | [`VolumesActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/volumes-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md).


# Example Usage

```java
int id = 112;
VolumesActionsChangeProtectionRequest body = new VolumesActionsChangeProtectionRequest.Builder()
    .delete(true)
    .build();

volumeActionsApi.changeVolumeProtectionAsync(id, body).thenAccept(result -> {
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
        "id": 42,
        "type": "server"
      },
      {
        "id": 554,
        "type": "volume"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



