# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `floatingIps` | [`FloatingIp[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ip.md) | Required | - | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FloatingIpsResponseBuilder;
use HetznerCloudApiLib\Models\Builders\FloatingIpBuilder;
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\HomeLocationBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Type16;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

$floatingIpsResponse = FloatingIpsResponseBuilder::init(
    [
        FloatingIpBuilder::init(
            false,
            '2016-01-30T23:55:00+00:00',
            [
                DnsPtrBuilder::init(
                    'server.example.com',
                    '2001:db8::1'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
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
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            42,
            '131.232.99.1',
            [
                'key0' => 'labels2'
            ],
            'my-resource',
            ProtectionBuilder::init(
                false
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Type16::IPV4
        )
            ->description('this describes my resource')
            ->server(42)
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



