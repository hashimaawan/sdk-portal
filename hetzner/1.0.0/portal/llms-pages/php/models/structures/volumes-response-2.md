# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type array.*


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/volume-1.md) | Required | - | getVolume(): Volume1 | setVolume(Volume1 volume): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\VolumesResponse2Builder;
use HetznerCloudApiLib\Models\Builders\Volume1Builder;
use HetznerCloudApiLib\Models\Builders\Location16Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Status113;

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
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        'my-resource',
        ProtectionBuilder::init(
            false
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        42,
        Status113::AVAILABLE
    )
        ->format('xfs')
        ->server(12)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



