# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU


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
| `prices` | [`Price[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/price.md) | Required | Prices in different network zones | getPrices(): array | setPrices(array prices): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudAPILib\Models\Builders\PriceBuilder;
use HetznerCloudAPILib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudAPILib\Models\Builders\PriceMonthlyBuilder;

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
            )->build(),
            PriceMonthlyBuilder::init(
                '1.1900000000000000',
                '1.0000000000'
            )->build()
        )->build()
    ]
)
    ->deprecated('2016-01-30T23:50:00+00:00')
    ->build();
```



