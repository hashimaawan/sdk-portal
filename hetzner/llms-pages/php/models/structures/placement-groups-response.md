# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `placementGroups` | [`PlacementGroup[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/placement-group.md) | Required | - | getPlacementGroups(): array | setPlacementGroups(array placementGroups): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PlacementGroupsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PlacementGroupBuilder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$placementGroupsResponse = PlacementGroupsResponseBuilder::init(
    [
        PlacementGroupBuilder::init(
            '2016-01-30T23:55:00+00:00',
            42,
            [
                'key0' => 'labels0',
                'key1' => 'labels1'
            ],
            'my-resource',
            [
                42
            ]
        )->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->build()
        )->build()
    )->build();
```



