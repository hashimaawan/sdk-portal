# Resize Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlZvbHVtZSUyNTIwQWN0aW9ucyUyRlJlc2l6ZSUyNTIwVm9sdW1l

Changes the size of a Volume. Note that downsizing a Volume is not possible.

:information_source: **Note** This endpoint does not require authentication.

```php
function resizeVolume(int $id, ?VolumesActionsResizeRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Volume |
| `body` | [`?VolumesActionsResizeRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/volumes-actions-resize-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `resize_volume` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md).


# Example Usage

```php
$id = 112;

$body = VolumesActionsResizeRequestBuilder::init(
    50
)->build();

$volumeActionsApi = $client->getVolumeActionsApi();
$apiResponse = $volumeActionsApi->resizeVolume(
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
    "command": "resize_volume",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": null,
    "id": 13,
    "progress": 0,
    "resources": [
      {
        "id": 554,
        "type": "volume"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



