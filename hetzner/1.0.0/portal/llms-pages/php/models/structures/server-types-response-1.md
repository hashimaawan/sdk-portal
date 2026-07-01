# Server Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNlMQ


# Class Name

`ServerTypesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `serverType` | [`ServerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-type.md) | Required | - | getServerType(): ServerType | setServerType(ServerType serverType): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerTypesResponse1Builder;
use HetznerCloudAPILib\Models\Builders\ServerTypeBuilder;
use HetznerCloudAPILib\Models\CpuTypeEnum;
use HetznerCloudAPILib\Models\Builders\Price9Builder;
use HetznerCloudAPILib\Models\Builders\PriceHourly8Builder;
use HetznerCloudAPILib\Models\Builders\PriceMonthly10Builder;
use HetznerCloudAPILib\Models\StorageTypeEnum;

$serverTypesResponse1 = ServerTypesResponse1Builder::init(
    ServerTypeBuilder::init(
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
)->build();
```



