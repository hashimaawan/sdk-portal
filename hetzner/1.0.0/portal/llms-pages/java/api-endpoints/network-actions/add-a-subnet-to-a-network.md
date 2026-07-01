# Add a Subnet to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZBZGQlMjUyMGElMjUyMHN1Ym5ldCUyNTIwdG8lMjUyMGElMjUyME5ldHdvcms

Adds a new subnet object to the Network. If you do not specify an `ip_range` for the subnet we will automatically pick the first available /24 range for you if possible.

Note: if the parent Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ActionResponse> addASubnetToANetworkAsync(
    final int id,
    final AddSubnetRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`AddSubnetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/add-subnet-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_subnet` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/action-response.md)


# Example Usage

```java
int id = 112;
AddSubnetRequest body = new AddSubnetRequest.Builder(
    "eu-central",
    Type42Enum.SERVER
)
.ipRange("10.0.1.0/24")
.vswitchId(1000)
.build();

networkActionsController.addASubnetToANetworkAsync(id, body).thenAccept(result -> {
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
    "command": "add_subnet",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 4711,
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



