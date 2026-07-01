# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`PrimaryIpResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `primaryIp` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-ip-1.md) | Required | - | getPrimaryIp(): PrimaryIp1 | setPrimaryIp(PrimaryIp1 primaryIp): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\PrimaryIpResponseBuilder;
use HetznerCloudApiLib\Models\Builders\PrimaryIp1Builder;
use HetznerCloudApiLib\Models\Builders\Datacenter2Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Type50;

$primaryIpResponse = PrimaryIpResponseBuilder::init(
    PrimaryIp1Builder::init(
        true,
        false,
        '2016-01-30T23:55:00+00:00',
        Datacenter2Builder::init(
            'Falkenstein DC Park 8',
            42,
            LocationBuilder::init(
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
            'fsn1-dc8',
            ServerTypesBuilder::init(
                [
                    1,
                    2,
                    3
                ],
                [
                    1,
                    2,
                    3
                ],
                [
                    1,
                    2,
                    3
                ]
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        [
            DnsPtrBuilder::init(
                'server.example.com',
                '2001:db8::1'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ],
        42,
        '131.232.99.1',
        [
            'key0' => 'labels2',
            'key1' => 'labels1'
        ],
        'my-resource',
        ProtectionBuilder::init(
            false
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        Type50::IPV4
    )
        ->assigneeId(17)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



