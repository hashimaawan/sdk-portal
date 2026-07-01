# Enable Rescue Mode for a Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlNlcnZlciUyNTIwQWN0aW9ucyUyRkVuYWJsZSUyNTIwUmVzY3VlJTI1MjBNb2RlJTI1MjBmb3IlMjUyMGElMjUyMFNlcnZlcg

Enable the Hetzner Rescue System for this Server. The next time a Server with enabled rescue mode boots it will start a special minimal Linux distribution designed for repair and reinstall.

In case a Server cannot boot on its own you can use this to access a Server’s disks.

Rescue Mode is automatically disabled when you first boot into it or if you do not use it for 60 minutes.

Enabling rescue mode will not [reboot](https://docs.hetzner.cloud/#server-actions-soft-reboot-a-server) your Server — you will have to do this yourself.

:information_source: **Note** This endpoint does not require authentication.

```php
function enableRescueModeForAServer(int $id, ?ServersActionsEnableRescueRequest $body = null): ApiResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Server |
| `body` | [`?ServersActionsEnableRescueRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-actions-enable-rescue-request.md) | Body, Optional | - |


# Response Type

**201**: The `root_password` key in the reply contains the root password that can be used to access the booted rescue system.

The `action` key in the reply contains an Action object with this structure

This method returns an [`ApiResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/sdk-infrastructure/utilities/apiresponse.md) instance. The `getResult()` method on this instance returns the response data which is of type [`ServersActionsEnableRescueResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/servers-actions-enable-rescue-response.md).


# Example Usage

```php
$id = 112;

$body = ServersActionsEnableRescueRequestBuilder::init()
    ->sshKeys(
        [
            2323
        ]
    )
    ->build();

$serverActionsApi = $client->getServerActionsApi();
$apiResponse = $serverActionsApi->enableRescueModeForAServer(
    $id,
    $body
);

// Extracting response status code
var_dump($apiResponse->getStatusCode());
// Extracting response headers
var_dump($apiResponse->getHeaders());

if ($apiResponse->isSuccess()) {
    echo 'ServersActionsEnableRescueResponse:';
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
    "command": "enable_rescue",
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
  },
  "root_password": "zCWbFhnu950dUTko5f40"
}
```



