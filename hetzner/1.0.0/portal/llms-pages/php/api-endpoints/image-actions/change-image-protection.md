# Change Image Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRkltYWdlJTI1MjBBY3Rpb25zJTJGQ2hhbmdlJTI1MjBJbWFnZSUyNTIwUHJvdGVjdGlvbg

Changes the protection configuration of the Image. Can only be used on snapshots.

:information_source: **Note** This endpoint does not require authentication.

```php
function changeImageProtection(int $id, ?ImagesActionsChangeProtectionRequest $body = null): ActionResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the Image |
| `body` | [`?ImagesActionsChangeProtectionRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/images-actions-change-protection-request.md) | Body, Optional | - |


# Response Type

**201**: The `action` key contains the `change_protection` Action

[`ActionResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action-response.md)


# Example Usage

```php
$id = 112;

$body = ImagesActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->build();

$imageActionsController = $client->getImageActionsController();

try {
    $result = $imageActionsController->changeImageProtection(
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
        "type": "image"
      }
    ],
    "started": "2016-01-30T23:55:00+00:00",
    "status": "success"
  }
}
```



