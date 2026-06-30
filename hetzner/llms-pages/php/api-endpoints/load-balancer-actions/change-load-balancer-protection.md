# Change Load Balancer Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBMb2FkJTI1MjBCYWxhbmNlciUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of a Load Balancer.

:information_source: **Note** This endpoint does not require authentication.

```php
function changeLoadBalancerProtection(
    int $id,
    ?LoadBalancersActionsChangeProtectionRequest $body = null
): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Load Balancer |
| `body` | [`?LoadBalancersActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/load-balancers-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$body = LoadBalancersActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->build();

$loadBalancerActionsController = $client->getLoadBalancerActionsController();

try {
    $result = $loadBalancerActionsController->changeLoadBalancerProtection(
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
    "command": "change_protection",
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



