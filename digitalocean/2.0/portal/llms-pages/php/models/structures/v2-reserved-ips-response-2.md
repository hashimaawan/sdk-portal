# V2 Reserved Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZXNlcnZlZCUyNTIwSXBzJTI1MjBSZXNwb25zZTI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ReservedIpsResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reservedIp` | [`?ReservedIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/reserved-ip.md) | Optional | - | getReservedIp(): ?ReservedIp | setReservedIp(?ReservedIp reservedIp): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ReservedIpsResponse2Builder;
use DigitalOceanApiLib\Models\Builders\ReservedIpBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;

$v2ReservedIpsResponse2 = V2ReservedIpsResponse2Builder::init()
    ->reservedIp(
        ReservedIpBuilder::init()
            ->droplet(
                ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
            )
            ->ip('ip6')
            ->locked(false)
            ->projectId('00002548-0000-0000-0000-000000000000')
            ->region(
                RegionBuilder::init(
                    false,
                    [
                        'features7',
                        'features8',
                        'features9'
                    ],
                    'name6',
                    [
                        'sizes6'
                    ],
                    'slug0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



