# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `floatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/floating-ip.md) | Required | - | getFloatingIp(): FloatingIp | setFloatingIp(FloatingIp floatingIp): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FloatingIpsResponse1Builder;
use HetznerCloudAPILib\Models\Builders\FloatingIpBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\HomeLocationBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type16Enum;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;

$floatingIpsResponse1 = FloatingIpsResponse1Builder::init(
    FloatingIpBuilder::init(
        false,
        '2016-01-30T23:55:00+00:00',
        [
            DnsPtrBuilder::init(
                'server.example.com',
                '2001:db8::1'
            )->build()
        ],
        HomeLocationBuilder::init(
            'Falkenstein',
            'DE',
            'Falkenstein DC Park 1',
            1,
            50.47612,
            12.370071,
            'fsn1',
            'eu-central'
        )->build(),
        42,
        '131.232.99.1',
        [
            'key0' => 'labels4',
            'key1' => 'labels3',
            'key2' => 'labels2'
        ],
        'my-resource',
        ProtectionBuilder::init(
            false
        )->build(),
        Type16Enum::IPV4
    )
        ->description('this describes my resource')
        ->server(42)
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



