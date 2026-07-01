# Remove Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGUmVtb3ZlJTI1MjBUYXJnZXQ

Removes a target from a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```php
function removeTarget(int $id, ?RemoveTargetRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`?RemoveTargetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/remove-target-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `remove_target` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md).


# Example Usage

```php
$id = 112;

$loadBalancerActionsApi = $client->getLoadBalancerActionsApi();
$apiResponse = $loadBalancerActionsApi->removeTarget($id);

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
    "command": "remove_target",
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



