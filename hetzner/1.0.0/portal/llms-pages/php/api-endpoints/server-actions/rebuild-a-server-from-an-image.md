# Rebuild a Server from an Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRlJlYnVpbGQlMjUyMGElMjUyMFNlcnZlciUyNTIwZnJvbSUyNTIwYW4lMjUyMEltYWdl

Rebuilds a Server overwriting its disk with the content of an Image, thereby **destroying all data** on the target Server

The Image can either be one you have created earlier (`backup` or `snapshot` Image) or it can be a completely fresh `system` Image provided by us. You can get a list of all available Images with `GET /images`.

Your Server will automatically be powered off before the rebuild command executes.

:information_source: **Note** This endpoint does not require authentication.

```php
function rebuildAServerFromAnImage(int $id, ?RebuildServerRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`?RebuildServerRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/rebuild-server-request.md) | Body, Optional | To select which Image to rebuild from you can either pass an ID or a name as the `image` argument. Passing a name only works for `system` Images since the other Image types do not have a name set. |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServersActionsRebuildResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-actions-rebuild-response.md).


# Example Usage

```php
$id = 112;

$body = RebuildServerRequestBuilder::init(
    'ubuntu-20.04'
)->build();

$serverActionsApi = $client->getServerActionsApi();
$apiResponse = $serverActionsApi->rebuildAServerFromAnImage(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServersActionsRebuildResponse:';
    var_dump($apiResponse->getResult());
} else {
    $error = $apiResponse->getResult();
    var_dump($error);
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



