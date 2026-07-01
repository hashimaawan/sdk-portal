# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/volume-1.md) | Required | - | getVolume(): Volume1 | setVolume(Volume1 volume): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumesResponse2Builder;
use HetznerCloudAPILib\Models\Builders\Volume1Builder;
use HetznerCloudAPILib\Models\Builders\Location16Builder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status113Enum;

$volumesResponse2 = VolumesResponse2Builder::init(
    Volume1Builder::init(
        '2016-01-30T23:55:00+00:00',
        42,
        [
            'key0' => 'labels8',
            'key1' => 'labels9',
            'key2' => 'labels0'
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
)->build();
```



