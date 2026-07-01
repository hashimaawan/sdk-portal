# Add Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQWRkJTI1MjBTZXJ2aWNl

Adds a service to a Load Balancer.

#### Call specific error codes

| Code                       | Description                                             |
|----------------------------|---------------------------------------------------------|
| `source_port_already_used` | The source port you are trying to add is already in use |

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ApiResponse<ActionResponse>> addServiceAsync(
    final int id,
    final LoadBalancerService body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`LoadBalancerService`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/load-balancer-service.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_service` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` getter of this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md).


# Example Usage

```java
int id = 112;
LoadBalancerService body = new LoadBalancerService.Builder(
    80,
    new LoadBalancerServiceHealthCheck.Builder(
        15,
        4711,
        Protocol6.HTTP,
        3,
        10
    )
    .build(),
    443,
    Protocol7.HTTPS,
    false
)
.build();

loadBalancerActionsApi.addServiceAsync(id, body).thenAccept(result -> {
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
    "command": "add_service",
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
        "type": "load_balancer"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



