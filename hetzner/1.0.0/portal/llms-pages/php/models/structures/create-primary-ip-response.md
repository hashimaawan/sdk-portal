# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl


# Class Name

`CreatePrimaryIPResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `primaryIp` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-ip-1.md) | Required | - | getPrimaryIp(): PrimaryIP1 | setPrimaryIp(PrimaryIP1 primaryIp): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreatePrimaryIPResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PrimaryIP1Builder;
use HetznerCloudAPILib\Models\Builders\Datacenter2Builder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type50Enum;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$createPrimaryIPResponse = CreatePrimaryIPResponseBuilder::init(
    PrimaryIP1Builder::init(
        true,
        false,
        '2016-01-30T23:55:00+00:00',
        Datacenter2Builder::init(
            'Falkenstein DC Park 8',
            42,
            LocationBuilder::init(
                'Falkenstein',
                'DE',
                'Falkenstein DC Park 1',
                1,
                50.47612,
                12.370071,
                'fsn1',
                'eu-central'
            )->build(),
            'fsn1-dc8',
            ServerTypesBuilder::init(
                [
                    1,
                    2,
                    3
                ],
                [
                    1,
                    2,
                    3
                ],
                [
                    1,
                    2,
                    3
                ]
            )->build()
        )->build(),
        [
            DnsPtrBuilder::init(
                'server.example.com',
                '2001:db8::1'
            )->build()
        ],
        42,
        '131.232.99.1',
        [
            'key0' => 'labels2',
            'key1' => 'labels1'
        ],
        'my-resource',
        ProtectionBuilder::init(
            false
        )->build(),
        Type50Enum::IPV4
    )
        ->assigneeId(17)
        ->build()
)
    ->action(
        ActionBuilder::init(
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



