# Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3VwUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`PlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group.md) | Required | - | getPlacementGroup(): PlacementGroup | setPlacementGroup(PlacementGroup placementGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PlacementGroupResponseBuilder;
use HetznerCloudApiLib\Models\Builders\PlacementGroupBuilder;
use HetznerCloudApiLib\ApiHelper;

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
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



