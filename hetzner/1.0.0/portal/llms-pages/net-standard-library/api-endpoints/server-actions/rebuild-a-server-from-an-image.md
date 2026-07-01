# Rebuild a Server from an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlJlYnVpbGQlMjUyMGElMjUyMFNlcnZlciUyNTIwZnJvbSUyNTIwYW4lMjUyMEltYWdl

Rebuilds a Server overwriting its disk with the content of an Image, thereby **destroying all data** on the target Server

The Image can either be one you have created earlier (`backup` or `snapshot` Image) or it can be a completely fresh `system` Image provided by us. You can get a list of all available Images with `GET /images`.

Your Server will automatically be powered off before the rebuild command executes.

:information_source: **Note** This endpoint does not require authentication.

```csharp
RebuildAServerFromAnImageAsync(
    int id,
    Models.RebuildServerRequest body = null)
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`RebuildServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/rebuild-server-request.md) | Body, Optional | To select which Image to rebuild from you can either pass an ID or a name as the `image` argument. Passing a name only works for `system` Images since the other Image types do not have a name set. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/sdk-infrastructure/utilities/apiresponse.md) instance. The `Data` property of this instance returns the response data which is of type [Models.ServersActionsRebuildResponse](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/servers-actions-rebuild-response.md).


# Example Usage

```csharp
int id = 112;
RebuildServerRequest body = new RebuildServerRequest
{
    Image = "ubuntu-20.04",
};

try
{
    ApiResponse<ServersActionsRebuildResponse> result = await serverActionsApi.RebuildAServerFromAnImageAsync(
        id,
        body
    );
}
catch (ApiException e)
{
    Console.WriteLine(e.Message);
}
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



