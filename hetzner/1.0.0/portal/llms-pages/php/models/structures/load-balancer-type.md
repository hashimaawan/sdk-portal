# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `deprecated` | `?string` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) | getDeprecated(): ?string | setDeprecated(?string deprecated): void |
| `description` | `string` | Required | Description of the Load Balancer type | getDescription(): string | setDescription(string description): void |
| `id` | `float` | Required | ID of the Load Balancer type | getId(): float | setId(float id): void |
| `maxAssignedCertificates` | `float` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer | getMaxAssignedCertificates(): float | setMaxAssignedCertificates(float maxAssignedCertificates): void |
| `maxConnections` | `float` | Required | Number of maximum simultaneous open connections | getMaxConnections(): float | setMaxConnections(float maxConnections): void |
| `maxServices` | `float` | Required | Number of services a Load Balancer of this type can have | getMaxServices(): float | setMaxServices(float maxServices): void |
| `maxTargets` | `float` | Required | Number of targets a single Load Balancer can have | getMaxTargets(): float | setMaxTargets(float maxTargets): void |
| `name` | `string` | Required | Unique identifier of the Load Balancer type | getName(): string | setName(string name): void |
| `prices` | [`Price[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/price.md) | Required | Prices in different network zones | getPrices(): array | setPrices(array prices): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudApiLib\Models\Builders\PriceBuilder;
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\PriceMonthlyBuilder;

$loadBalancerType = LoadBalancerTypeBuilder::init(
    'LB11',
    1,
    10,
    20000,
    5,
    25,
    'lb11',
    [
        PriceBuilder::init(
            'fsn1',
            PriceHourlyBuilder::init(
                '1.1900000000000000',
                '1.0000000000'
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            PriceMonthlyBuilder::init(
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
    ->deprecated('2016-01-30T23:50:00+00:00')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



