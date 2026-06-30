# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `serverTypes` | [`ServerTypes7[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-types-7.md) | Required | - | getServerTypes(): array | setServerTypes(array serverTypes): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerTypesResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ServerTypes7Builder;
use HetznerCloudAPILib\Models\CpuTypeEnum;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudAPILib\Models\StorageTypeEnum;

$serverTypesResponse = ServerTypesResponseBuilder::init(
    [
        ServerTypes7Builder::init(
            1,
            CpuTypeEnum::SHARED,
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
                    )->build(),
                    PriceMonthly10Builder::init(
                        '1.1900000000000000',
                        '1.0000000000'
                    )->build()
                )->build()
            ],
            StorageTypeEnum::LOCAL
        )->build()
    ]
)->build();
```



