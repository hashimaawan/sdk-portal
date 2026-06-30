# Change Primary IP Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBQcmltYXJ5JTI1MjBJUCUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of a Primary IP.

A Primary IP can only be delete protected if its `auto_delete` property is set to `false`.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> changePrimaryIPProtectionAsync(
    final int id,
    final ChangeProtectionRequest2 body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |
| `body` | [`ChangeProtectionRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/change-protection-request-2.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
ChangeProtectionRequest2 body = new ChangeProtectionRequest2.Builder()
    .delete(true)
    .build();

primaryIPActionsController.changePrimaryIPProtectionAsync(id, body).thenAccept(result -> {
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
        "type": "primary_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



