# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl


# Class Name

`PrimaryIPResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `primaryIp` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/primary-ip-1.md) | Required | - | getPrimaryIp(): PrimaryIP1 | setPrimaryIp(PrimaryIP1 primaryIp): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrimaryIPResponseBuilder;
use HetznerCloudAPILib\Models\Builders\PrimaryIP1Builder;
use HetznerCloudAPILib\Models\Builders\Datacenter2Builder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypesBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type50Enum;

$primaryIPResponse = PrimaryIPResponseBuilder::init(
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
)->build();
```



