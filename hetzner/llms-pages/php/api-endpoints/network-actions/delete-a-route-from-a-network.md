# Delete a Route from a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRk5ldHdvcmslMjUyMEFjdGlvbnMlMkZEZWxldGUlMjUyMGElMjUyMHJvdXRlJTI1MjBmcm9tJTI1MjBhJTI1MjBOZXR3b3Jr

Delete a route entry from a Network.

Note: if the Network object changes during the request, the response will be a “conflict” error.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteARouteFromANetwork(int $id, ?AddDeleteRouteRequest $body = null): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Network |
| `body` | [`?AddDeleteRouteRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/add-delete-route-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `delete_route` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$body = AddDeleteRouteRequestBuilder::init(
    '10.100.1.0/24',
    '10.0.1.1'
)->build();

$networkActionsController = $client->getNetworkActionsController();

try {
    $result = $networkActionsController->deleteARouteFromANetwork(
        $id,
        $body
    );
    echo 'ActionResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Example Response *(as JSON)*

```json
{
  "action": {
    "command": "delete_route",
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



