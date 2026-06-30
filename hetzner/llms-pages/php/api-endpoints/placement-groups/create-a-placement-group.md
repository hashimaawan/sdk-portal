# Create a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGQ3JlYXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Creates a new PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```php
function createAPlacementGroup(?CreatePlacementGroupRequest $body = null): CreatePlacementGroupResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`?CreatePlacementGroupRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/create-placement-group-request.md) | Body, Optional | - |


# Response Type

**201**: The `PlacementGroup` key contains the PlacementGroup that was just created.

[`CreatePlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/create-placement-group-response.md)


# Example Usage

```php
$body = CreatePlacementGroupRequestBuilder::init(
    'my Placement Group'
)->build();

$placementGroupsController = $client->getPlacementGroupsController();

try {
    $result = $placementGroupsController->createAPlacementGroup($body);
    echo 'CreatePlacementGroupResponse:';
    var_dump($result);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```


# Example Response *(as JSON)*

```json
{
  "placement_group": {
    "created": "2019-01-08T12:10:00+00:00",
    "id": 897,
    "labels": {
      "key": "value"
    },
    "name": "my Placement Group",
    "servers": [],
    "type": "spread"
  }
}
```



