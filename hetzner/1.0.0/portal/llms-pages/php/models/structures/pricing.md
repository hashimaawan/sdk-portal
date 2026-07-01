# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 | getCurrency(): string | setCurrency(string currency): void |
| `floatingIp` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month | getFloatingIp(): FloatingIp4 | setFloatingIp(FloatingIp4 floatingIp): void |
| `floatingIps` | [`FloatingIp5[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image-3.md) | Required | The cost of Image per GB/month | getImage(): Image3 | setImage(Image3 image): void |
| `loadBalancerTypes` | [`LoadBalancerType6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type | getLoadBalancerTypes(): array | setLoadBalancerTypes(array loadBalancerTypes): void |
| `primaryIps` | [`PrimaryIp[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location | getPrimaryIps(): array | setPrimaryIps(array primaryIps): void |
| `serverBackup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage | getServerBackup(): ServerBackup | setServerBackup(ServerBackup serverBackup): void |
| `serverTypes` | [`ServerTypes2[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type | getServerTypes(): array | setServerTypes(array serverTypes): void |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/traffic.md) | Required | The cost of additional traffic per TB | getTraffic(): Traffic | setTraffic(Traffic traffic): void |
| `vatRate` | `string` | Required | The VAT rate used for calculating prices with VAT | getVatRate(): string | setVatRate(string vatRate): void |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/volume.md) | Required | The cost of Volume per GB/month | getVolume(): Volume | setVolume(Volume volume): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PricingBuilder;
use HetznerCloudApiLib\Models\Builders\FloatingIp4Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly6Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\FloatingIp5Builder;
use HetznerCloudApiLib\Models\Builders\Price6Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly7Builder;
use HetznerCloudApiLib\Models\Type48;
use HetznerCloudApiLib\Models\Builders\Image3Builder;
use HetznerCloudApiLib\Models\Builders\PricePerGbMonthBuilder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerType6Builder;
use HetznerCloudApiLib\Models\Builders\Price7Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly6Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly8Builder;
use HetznerCloudApiLib\Models\Builders\PrimaryIpBuilder;
use HetznerCloudApiLib\Models\Builders\Price8Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly7Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly9Builder;
use HetznerCloudApiLib\Models\Type49;
use HetznerCloudApiLib\Models\Builders\ServerBackupBuilder;
use HetznerCloudApiLib\Models\Builders\ServerTypes2Builder;
use HetznerCloudApiLib\Models\Builders\Price9Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly8Builder;
use HetznerCloudApiLib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudApiLib\Models\Builders\TrafficBuilder;
use HetznerCloudApiLib\Models\Builders\PricePerTbBuilder;
use HetznerCloudApiLib\Models\Builders\VolumeBuilder;

$pricing = PricingBuilder::init(
    'EUR',
    FloatingIp4Builder::init(
        PriceMonthly6Builder::init(
            '1.1900000000000000',
            '1.0000000000'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        FloatingIp5Builder::init(
            [
                Price6Builder::init(
                    'fsn1',
                    PriceMonthly7Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            Type48::IPV4
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    Image3Builder::init(
        PricePerGbMonthBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        LoadBalancerType6Builder::init(
            1,
            'lb11',
            [
                Price7Builder::init(
                    'fsn1',
                    PriceHourly6Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthly8Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    [
        PrimaryIpBuilder::init(
            [
                Price8Builder::init(
                    'fsn1',
                    PriceHourly7Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthly9Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            Type49::IPV4
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    ServerBackupBuilder::init(
        '20.0000000000'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        ServerTypes2Builder::init(
            4,
            'cx11',
            [
                Price9Builder::init(
                    'fsn1',
                    PriceHourly8Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    PriceMonthly10Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    TrafficBuilder::init(
        PricePerTbBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    '19.000000',
    VolumeBuilder::init(
        PricePerGbMonthBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)->build();
```



