# Change Server Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkNoYW5nZSUyNTIwU2VydmVyJTI1MjBQcm90ZWN0aW9u

Changes the protection configuration of the Server.

:information_source: **Note** This endpoint does not require authentication.

```php
function changeServerProtection(int $id, ?ServersActionsChangeProtectionRequest $body = null): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`?ServersActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$body = ServersActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->rebuild(true)
    ->build();

$serverActionsController = $client->getServerActionsController();

try {
    $result = $serverActionsController->changeServerProtection(
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
        "id": 42,
        "type": "server"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



