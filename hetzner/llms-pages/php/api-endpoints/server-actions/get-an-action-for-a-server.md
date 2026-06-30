# Get an Action for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkdldCUyNTIwYW4lMjUyMEFjdGlvbiUyNTIwZm9yJTI1MjBhJTI1MjBTZXJ2ZXI

Returns a specific Action object for a Server.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAnActionForAServer(int $id, int $actionId): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `actionId` | `int` | Template, Required | ID of the Action |


# Response Type

**200**: The `action` key in the reply has this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$actionId = 224;

$serverActionsController = $client->getServerActionsController();

try {
    $result = $serverActionsController->getAnActionForAServer(
        $id,
        $actionId
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
    "command": "start_server",
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



