# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `floatingIps` | [`FloatingIp[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/floating-ip.md) | Required | - | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FloatingIpsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\FloatingIpBuilder;
use HetznerCloudAPILib\Models\Builders\DnsPtrBuilder;
use HetznerCloudAPILib\Models\Builders\HomeLocationBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Type16Enum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$floatingIpsResponse = FloatingIpsResponseBuilder::init(
    [
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
                'key0' => 'labels2'
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



