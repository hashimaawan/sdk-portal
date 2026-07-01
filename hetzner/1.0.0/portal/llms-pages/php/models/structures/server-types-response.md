# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `serverTypes` | [`ServerTypes7[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-types-7.md) | Required | - | getServerTypes(): array | setServerTypes(array serverTypes): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServerTypesResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ServerTypes7Builder;
use HetznerCloudApiLib\Models\CpuType;
use HetznerCloudApiLib\Models\Builders\Price9Builder;
use HetznerCloudApiLib\Models\Builders\PriceHourly8Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudApiLib\Models\StorageType;

$serverTypesResponse = ServerTypesResponseBuilder::init(
    [
        ServerTypes7Builder::init(
            1,
            CpuType::SHARED,
            false,
            'CX11',
            24,
            1,
            1,
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
            ],
            StorageType::LOCAL
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



