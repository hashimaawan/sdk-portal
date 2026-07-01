# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group.md) | Required | - | getPlacementGroup(): PlacementGroup | setPlacementGroup(PlacementGroup placementGroup): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PlacementGroupResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PlacementGroupBuilder;

$placementGroupResponse = PlacementGroupResponseBuilder::init(
    PlacementGroupBuilder::init(
        '2016-01-30T23:55:00+00:00',
        42,
        [
            'key0' => 'labels4'
        ],
        'my-resource',
        [
            42
        ]
    )->build()
)->build();
```



