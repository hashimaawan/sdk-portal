# Add Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQWRkJTI1MjBUYXJnZXQ

Adds a target to a Load Balancer.

#### Call specific error codes

| Code                                    | Description                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------|
| `cloud_resource_ip_not_allowed`         | The IP you are trying to add as a target belongs to a Hetzner Cloud resource                          |
| `ip_not_owned`                          | The IP you are trying to add as a target is not owned by the Project owner                            |
| `load_balancer_not_attached_to_network` | The Load Balancer is not attached to a network                                                        |
| `robot_unavailable`                     | Robot was not available. The caller may retry the operation after a short delay.                      |
| `server_not_attached_to_network`        | The server you are trying to add as a target is not attached to the same network as the Load Balancer |
| `target_already_defined`                | The Load Balancer target you are trying to define is already defined                                  |

:information_source: **Note** This endpoint does not require authentication.

```php
function addTarget(int $id, ?AddTargetRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`?AddTargetRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/add-target-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `add_target` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md).


# Example Usage

```php
$id = 112;

$body = AddTargetRequestBuilder::init(
    Type29::LABEL_SELECTOR
)
    ->usePrivateIp(true)
    ->build();

$loadBalancerActionsApi = $client->getLoadBalancerActionsApi();
$apiResponse = $loadBalancerActionsApi->addTarget(
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
    "command": "add_target",
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



