# Detach a Server from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkRldGFjaCUyNTIwYSUyNTIwU2VydmVyJTI1MjBmcm9tJTI1MjBhJTI1MjBOZXR3b3Jr

Detaches a Server from a network. The interface for this network will vanish.

:information_source: **Note** This endpoint does not require authentication.

```php
function detachAServerFromANetwork(int $id, ?DetachFromNetworkRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`?DetachFromNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/detach-from-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md).


# Example Usage

```php
$id = 112;

$body = DetachFromNetworkRequestBuilder::init(
    4711
)->build();

$serverActionsApi = $client->getServerActionsApi();
$apiResponse = $serverActionsApi->detachAServerFromANetwork(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ActionResponse:';
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
    "command": "detach_from_network",
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
        "type": "network"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



