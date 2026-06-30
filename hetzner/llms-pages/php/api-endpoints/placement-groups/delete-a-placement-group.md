# Delete a Placement Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0ZSUyRlBsYWNlbWVudCUyNTIwR3JvdXBzJTJGRGVsZXRlJTI1MjBhJTI1MjBQbGFjZW1lbnRHcm91cA

Deletes a PlacementGroup.

:information_source: **Note** This endpoint does not require authentication.

```php
function deleteAPlacementGroup(int $id): void
```


# Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `int` | Template, Required | ID of the resource |


# Response Type

**204**: PlacementGroup deleted

`void`


# Example Usage

```php
$id = 112;

$placementGroupsController = $client->getPlacementGroupsController();

try {
    $placementGroupsController->deleteAPlacementGroup($id);
} catch (ApiException $exp) {
    echo 'Caught:', $exp;
}
```



