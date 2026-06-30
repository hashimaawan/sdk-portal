# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `currency` | `string` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 | getCurrency(): string | setCurrency(string currency): void |
| `floatingIp` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month | getFloatingIp(): FloatingIp4 | setFloatingIp(FloatingIp4 floatingIp): void |
| `floatingIps` | [`FloatingIp5[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type | getFloatingIps(): array | setFloatingIps(array floatingIps): void |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/image-3.md) | Required | The cost of Image per GB/month | getImage(): Image3 | setImage(Image3 image): void |
| `loadBalancerTypes` | [`LoadBalancerType6[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type | getLoadBalancerTypes(): array | setLoadBalancerTypes(array loadBalancerTypes): void |
| `primaryIps` | [`PrimaryIp[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location | getPrimaryIps(): array | setPrimaryIps(array primaryIps): void |
| `serverBackup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage | getServerBackup(): ServerBackup | setServerBackup(ServerBackup serverBackup): void |
| `serverTypes` | [`ServerTypes2[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type | getServerTypes(): array | setServerTypes(array serverTypes): void |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/traffic.md) | Required | The cost of additional traffic per TB | getTraffic(): Traffic | setTraffic(Traffic traffic): void |
| `vatRate` | `string` | Required | The VAT rate used for calculating prices with VAT | getVatRate(): string | setVatRate(string vatRate): void |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/volume.md) | Required | The cost of Volume per GB/month | getVolume(): Volume | setVolume(Volume volume): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PricingBuilder;
use HetznerCloudAPILib\Models\Builders\FloatingIp4Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly6Builder;
use HetznerCloudAPILib\Models\Builders\FloatingIp5Builder;
use HetznerCloudAPILib\Models\Builders\Price6Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly7Builder;
use HetznerCloudAPILib\Models\Type48Enum;
use HetznerCloudAPILib\Models\Builders\Image3Builder;
use HetznerCloudAPILib\Models\Builders\PricePerGbMonthBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerType6Builder;
use HetznerCloudAPILib\Models\Builders\Price7Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly6Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly8Builder;
use HetznerCloudAPILib\Models\Builders\PrimaryIpBuilder;
use HetznerCloudAPILib\Models\Builders\Price8Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly7Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly9Builder;
use HetznerCloudAPILib\Models\Type49Enum;
use HetznerCloudAPILib\Models\Builders\ServerBackupBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypes2Builder;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudAPILib\Models\Builders\TrafficBuilder;
use HetznerCloudAPILib\Models\Builders\PricePerTbBuilder;
use HetznerCloudAPILib\Models\Builders\VolumeBuilder;

$pricing = PricingBuilder::init(
    'EUR',
    FloatingIp4Builder::init(
        PriceMonthly6Builder::init(
            '1.1900000000000000',
            '1.0000000000'
        )->build()
    )->build(),
    [
        FloatingIp5Builder::init(
            [
                Price6Builder::init(
                    'fsn1',
                    PriceMonthly7Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ],
            Type48Enum::IPV4
        )->build()
    ],
    Image3Builder::init(
        PricePerGbMonthBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )->build()
    )->build(),
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
                    )->build(),
                    PriceMonthly8Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ]
        )->build()
    ],
    [
        PrimaryIpBuilder::init(
            [
                Price8Builder::init(
                    'fsn1',
                    PriceHourly7Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build(),
                    PriceMonthly9Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ],
            Type49Enum::IPV4
        )->build()
    ],
    ServerBackupBuilder::init(
        '20.0000000000'
    )->build(),
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
                    )->build(),
                    PriceMonthly10Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ]
        )->build()
    ],
    TrafficBuilder::init(
        PricePerTbBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )->build()
    )->build(),
    '19.000000',
    VolumeBuilder::init(
        PricePerGbMonthBuilder::init(
            '1.1900000000000000',
            '1.0000000000'
        )->build()
    )->build()
)->build();
```



