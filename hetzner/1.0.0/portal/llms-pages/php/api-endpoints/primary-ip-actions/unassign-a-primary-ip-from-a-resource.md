# Unassign a Primary IP from a Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlByaW1hcnklMjUyMElQJTI1MjBBY3Rpb25zJTJGVW5hc3NpZ24lMjUyMGElMjUyMFByaW1hcnklMjUyMElQJTI1MjBmcm9tJTI1MjBhJTI1MjByZXNvdXJjZQ

Unassigns a Primary IP from a Server.

The Server must be powered off (status `off`) in order for this operation to succeed.

Note that only Servers that have at least one network interface (public or private) attached can be powered on.

#### Call specific error codes

| Code                              | Description                                                   |
|---------------------------------- |-------------------------------------------------------------- |
| `server_not_stopped`              | The server is running, but needs to be powered off            |
| `server_is_load_balancer_target`  | The server ipv4 address is a loadbalancer target              |

:information_source: **Note** This endpoint does not require authentication.

```php
function unassignAPrimaryIPFromAResource(int $id): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Primary IP |


# Response Type

**201**: The `action` key in the reply contains an Action object with this structure

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$primaryIPActionsController = $client->getPrimaryIPActionsController();

try {
    $result = $primaryIPActionsController->unassignAPrimaryIPFromAResource($id);
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
    "command": "unassign_primary_ip",
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
        "type": "primary_ip"
      }
    ],
    "started": "2016-01-30T23:50:00+00:00",
    "status": "running"
  }
}
```



