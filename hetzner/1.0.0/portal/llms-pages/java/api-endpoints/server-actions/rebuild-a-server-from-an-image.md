# Rebuild a Server from an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlJlYnVpbGQlMjUyMGElMjUyMFNlcnZlciUyNTIwZnJvbSUyNTIwYW4lMjUyMEltYWdl

Rebuilds a Server overwriting its disk with the content of an Image, thereby **destroying all data** on the target Server

The Image can either be one you have created earlier (`backup` or `snapshot` Image) or it can be a completely fresh `system` Image provided by us. You can get a list of all available Images with `GET /images`.

Your Server will automatically be powered off before the rebuild command executes.

:information_source: **Note** This endpoint does not require authentication.

```java
CompletableFuture<ServersActionsRebuildResponse> rebuildAServerFromAnImageAsync(
    final int id,
    final RebuildServerRequest body)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`RebuildServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/rebuild-server-request.md) | Body, Optional | To select which Image to rebuild from you can either pass an ID or a name as the `image` argument. Passing a name only works for `system` Images since the other Image types do not have a name set. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ServersActionsRebuildResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/servers-actions-rebuild-response.md)


# Example Usage

```java
int id = 112;
RebuildServerRequest body = new RebuildServerRequest.Builder(
    "ubuntu-20.04"
)
.build();

serverActionsController.rebuildAServerFromAnImageAsync(id, body).thenAccept(result -> {
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
    "command": "rebuild_server",
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
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  },
  "root_password": null
}
```



