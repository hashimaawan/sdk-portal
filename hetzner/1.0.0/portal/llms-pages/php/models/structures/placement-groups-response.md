# Placement Groups Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlBsYWNlbWVudEdyb3Vwc1Jlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`PlacementGroupsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `placementGroups` | [`PlacementGroup[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/placement-group.md) | Required | - | getPlacementGroups(): array | setPlacementGroups(array placementGroups): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PlacementGroupsResponseBuilder;
use HetznerCloudApiLib\Models\Builders\PlacementGroupBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

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
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



