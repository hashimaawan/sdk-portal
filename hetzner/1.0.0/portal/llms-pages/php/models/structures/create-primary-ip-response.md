# Create Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`CreatePrimaryIpResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `primaryIp` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/primary-ip-1.md) | Required | - | getPrimaryIp(): PrimaryIp1 | setPrimaryIp(PrimaryIp1 primaryIp): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreatePrimaryIpResponseBuilder;
use HetznerCloudApiLib\Models\Builders\PrimaryIp1Builder;
use HetznerCloudApiLib\Models\Builders\Datacenter2Builder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;
use HetznerCloudApiLib\Models\Builders\DnsPtrBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Type50;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;

$createPrimaryIpResponse = CreatePrimaryIpResponseBuilder::init(
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
    ->action(
        ActionBuilder::init(
            'command6',
            238,
            143.26,
            [
                Resource2Builder::init(
                    198,
                    'type0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            'started8',
            Status::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->finished('finished0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



