# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Class Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `volumes` | [`Volume1[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/volume-1.md) | Required | - | getVolumes(): array | setVolumes(array volumes): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumesResponseBuilder;
use HetznerCloudAPILib\Models\Builders\Volume1Builder;
use HetznerCloudAPILib\Models\Builders\Location16Builder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status113Enum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$volumesResponse = VolumesResponseBuilder::init(
    [
        Volume1Builder::init(
            '2016-01-30T23:55:00+00:00',
            42,
            [
                'key0' => 'labels4'
            ],
            '/dev/disk/by-id/scsi-0HC_Volume_4711',
            Location16Builder::init(
                'Falkenstein',
                'DE',
                'Falkenstein DC Park 1',
                1,
                50.47612,
                12.370071,
                'fsn1',
                'eu-central'
            )->build(),
            'my-resource',
            ProtectionBuilder::init(
                false
            )->build(),
            42,
            Status113Enum::AVAILABLE
        )
            ->format('xfs')
            ->server(12)
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
                ->build()
        )->build()
    )->build();
```



