# Datacenters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFjZW50ZXJzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`DatacentersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `datacenters` | [`Datacenter[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/datacenter.md) | Required | - | getDatacenters(): array | setDatacenters(array datacenters): void |
| `recommendation` | `float` | Required | The Datacenter which is recommended to be used to create new Servers. | getRecommendation(): float | setRecommendation(float recommendation): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\DatacentersResponseBuilder;
use HetznerCloudApiLib\Models\Builders\DatacenterBuilder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\ServerTypesBuilder;

$datacentersResponse = DatacentersResponseBuilder::init(
    [
        DatacenterBuilder::init(
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
            ->build()
    ],
    1
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



