# Create Placement Group Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVBsYWNlbWVudEdyb3VwUmVzcG9uc2U


# Class Name

`CreatePlacementGroupResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/nullable-action.md) | Optional | - | getAction(): ?NullableAction | setAction(?NullableAction action): void |
| `placementGroup` | [`PlacementGroup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group.md) | Required | - | getPlacementGroup(): PlacementGroup | setPlacementGroup(PlacementGroup placementGroup): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreatePlacementGroupResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PlacementGroupBuilder;
use HetznerCloudAPILib\Models\Builders\NullableActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$createPlacementGroupResponse = CreatePlacementGroupResponseBuilder::init(
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
)
    ->action(
        NullableActionBuilder::init(
            'command6',
            238,
            143.26,
            [
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build()
            ],
            'started8',
            StatusEnum::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )->build()
            )
            ->finished('finished0')
            ->build()
    )
    ->build();
```



