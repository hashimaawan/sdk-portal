# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action.md) | Required | - | getAction(): Action | setAction(Action action): void |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action.md) | Required | - | getNextActions(): array | setNextActions(array nextActions): void |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/volume-1.md) | Required | - | getVolume(): Volume1 | setVolume(Volume1 volume): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\VolumesResponse1Builder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;
use HetznerCloudAPILib\Models\Builders\Volume1Builder;
use HetznerCloudAPILib\Models\Builders\Location16Builder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status113Enum;

$volumesResponse1 = VolumesResponse1Builder::init(
    ActionBuilder::init(
        'start_server',
        42,
        100,
        [
            Resource2Builder::init(
                42,
                'server'
            )->build()
        ],
        '2016-01-30T23:55:00+00:00',
        StatusEnum::RUNNING
    )
        ->error(
            ErrorBuilder::init(
                'action_failed',
                'Action failed'
            )->build()
        )
        ->finished('2016-01-30T23:55:00+00:00')
        ->build(),
    [
        ActionBuilder::init(
            'start_server',
            42,
            100,
            [
                Resource2Builder::init(
                    42,
                    'server'
                )->build()
            ],
            '2016-01-30T23:55:00+00:00',
            StatusEnum::SUCCESS
        )
            ->error(
                ErrorBuilder::init(
                    'action_failed',
                    'Action failed'
                )->build()
            )
            ->finished('2016-01-30T23:55:00+00:00')
            ->build()
    ],
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



