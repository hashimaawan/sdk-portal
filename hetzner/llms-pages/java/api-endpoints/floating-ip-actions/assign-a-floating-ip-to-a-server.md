# Assign a Floating IP to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkFzc2lnbiUyNTIwYSUyNTIwRmxvYXRpbmclMjUyMElQJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Assigns a Floating IP to a Server.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> assignAFloatingIPToAServerAsync(
    final int id,
    final AssignFloatingIPRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`AssignFloatingIPRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/assign-floating-ip-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `assign` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
AssignFloatingIPRequest body = new AssignFloatingIPRequest.Builder(
    42
)
.build();

floatingIPActionsController.assignAFloatingIPToAServerAsync(id, body).thenAccept(result -> {
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



