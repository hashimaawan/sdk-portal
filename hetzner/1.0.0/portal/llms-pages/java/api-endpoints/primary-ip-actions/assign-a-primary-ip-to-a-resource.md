# Assign a Primary IP to a Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGQXNzaWduJTI1MjBhJTI1MjBQcmltYXJ5JTI1MjBJUCUyNTIwdG8lMjUyMGElMjUyMHJlc291cmNl

Assigns a Primary IP to a Server.

A Server can only have one Primary IP of type `ipv4` and one of type `ipv6` assigned. If you need more IPs use Floating IPs.

The Server must be powered off (status `off`) in order for this operation to succeed.

#### Call specific error codes

| Code                          | Description                                                   |
|------------------------------ |-------------------------------------------------------------- |
| `server_not_stopped`          | The server is running, but needs to be powered off            |
| `primary_ip_already_assigned` | Primary ip is already assigned to a different server          |
| `server_has_ipv4`             | The server already has an ipv4 address                        |
| `server_has_ipv6`             | The server already has an ipv6 address                        |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionResponse>> assignAPrimaryIpToAResourceAsync(
    final int id,
    final AssignPrimaryIpRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |
| `body` | [`AssignPrimaryIpRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/assign-primary-ip-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md).


# Example Usage

```java
int id = 112;
AssignPrimaryIpRequest body = new AssignPrimaryIpRequest.Builder(
    4711,
    "server"
)
.build();

primaryIpActionsApi.assignAPrimaryIpToAResourceAsync(id, body).thenAccept(result -> {
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
    "command": "assign_primary_ip",
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
      },
      {
        "id": 4711,
        "type": "primary_ip"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



