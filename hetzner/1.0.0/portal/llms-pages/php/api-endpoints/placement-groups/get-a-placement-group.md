# Get a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGR2V0JTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Gets a specific PlacementGroup object.

:information_source: **Note** This endpoint does not require authentication.

```php
function getAPlacementGroup(int $id): PlacementGroupResponse
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**200**: The `placement_group` key contains a PlacementGroup object

[`PlacementGroupResponse`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group-response.md)


# Example Usage

```php
$id = 112;

$placementGroupsController = $client->getPlacementGroupsController();

try {
    $result = $placementGroupsController->getAPlacementGroup($id);
    echo 'PlacementGroupResponse:';
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
    "servers": [
      4711,
      4712
    ],
    "type": "spread"
  }
}
```



