# Assign a Floating IP to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkFzc2lnbiUyNTIwYSUyNTIwRmxvYXRpbmclMjUyMElQJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Assigns a Floating IP to a Server.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionResponse>> assignAFloatingIpToAServerAsync(
    final int id,
    final AssignFloatingIpRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`AssignFloatingIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/assign-floating-ip-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `assign` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md).


# Example Usage

```java
int id = 112;
AssignFloatingIpRequest body = new AssignFloatingIpRequest.Builder(
    42
)
.build();

floatingIpActionsApi.assignAFloatingIpToAServerAsync(id, body).thenAccept(result -> {
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



