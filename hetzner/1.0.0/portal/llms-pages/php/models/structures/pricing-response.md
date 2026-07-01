# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/pricing.md) | Required | - | getPricing(): Pricing | setPricing(Pricing pricing): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PricingResponseBuilder;
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

$pricingResponse = PricingResponseBuilder::init(
    PricingBuilder::init(
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
    )->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



