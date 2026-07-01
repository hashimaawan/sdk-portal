# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/pricing.md) | Required | - | getPricing(): Pricing | setPricing(Pricing pricing): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PricingResponseBuilder;
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

$pricingResponse = PricingResponseBuilder::init(
    PricingBuilder::init(
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
    )->build()
)->build();
```



