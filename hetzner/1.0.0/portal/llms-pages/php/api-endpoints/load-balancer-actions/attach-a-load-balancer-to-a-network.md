# Attach a Load Balancer to a Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQXR0YWNoJTI1MjBhJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwdG8lMjUyMGElMjUyME5ldHdvcms

Attach a Load Balancer to a Network.

**Call specific error codes**

| Code                             | Description                                                           |
|----------------------------------|-----------------------------------------------------------------------|
| `load_balancer_already_attached` | The Load Balancer is already attached to a network                    |
| `ip_not_available`               | The provided Network IP is not available                              |
| `no_subnet_available`            | No Subnet or IP is available for the Load Balancer within the network |

:information_source: **Note** This endpoint does not require authentication.

```php
function attachALoadBalancerToANetwork(
    int $id,
    ?LoadBalancersActionsAttachToNetworkRequest $body = null
): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`?LoadBalancersActionsAttachToNetworkRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancers-actions-attach-to-network-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `attach_to_network` Action

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md).


# Example Usage

```php
$id = 112;

$body = LoadBalancersActionsAttachToNetworkRequestBuilder::init(
    4711
)
    ->ip('10.0.1.1')
    ->build();

$loadBalancerActionsApi = $client->getLoadBalancerActionsApi();
$apiResponse = $loadBalancerActionsApi->attachALoadBalancerToANetwork(
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
    "command": "attach_to_network",
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



