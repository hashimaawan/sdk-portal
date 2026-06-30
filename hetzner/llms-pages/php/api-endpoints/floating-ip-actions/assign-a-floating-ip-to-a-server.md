# Assign a Floating IP to a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRkZsb2F0aW5nJTI1MjBJUCUyNTIwQWN0aW9ucyUyRkFzc2lnbiUyNTIwYSUyNTIwRmxvYXRpbmclMjUyMElQJTI1MjB0byUyNTIwYSUyNTIwU2VydmVy

Assigns a Floating IP to a Server.

:information_source: **Note** This endpoint does not require authentication.

```php
function assignAFloatingIPToAServer(int $id, ?AssignFloatingIPRequest $body = null): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Floating IP |
| `body` | [`?AssignFloatingIPRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/assign-floating-ip-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `assign` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$body = AssignFloatingIPRequestBuilder::init(
    42
)->build();

$floatingIPActionsController = $client->getFloatingIPActionsController();

try {
    $result = $floatingIPActionsController->assignAFloatingIPToAServer(
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
    "command": "assign_floating_ip",
    "error": {
      "code": "action_failed",
      "message": "Action failed"
    },
    "finished": "2016-01-30T23:56:00+00:00",
    "id": 13,
    "progress": 100,
    "resources": [
      {
        "id": 42,
        "type": "server"
      },
      {
        "id": 4711,
        "type": "floating_ip"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



