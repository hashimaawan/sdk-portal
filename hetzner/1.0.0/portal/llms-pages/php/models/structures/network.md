# Network

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRk5ldHdvcms


# Class Name

`Network`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `created` | `string` | Required | Point in time when the Network was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `id` | `int` | Required | ID of the Network | getId(): int | setId(int id): void |
| `ipRange` | `string` | Required | IPv4 prefix of the whole Network | getIpRange(): string | setIpRange(string ipRange): void |
| `labels` | `array` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `loadBalancers` | `?(int[])` | Optional | Array of IDs of Load Balancers attached to this Network | getLoadBalancers(): ?array | setLoadBalancers(?array loadBalancers): void |
| `name` | `string` | Required | Name of the Network | getName(): string | setName(string name): void |
| `protection` | [`Protection11`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection-11.md) | Required | Protection configuration for the Network | getProtection(): Protection11 | setProtection(Protection11 protection): void |
| `routes` | [`Route[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/route.md) | Required | Array of routes set in this Network | getRoutes(): array | setRoutes(array routes): void |
| `servers` | `int[]` | Required | Array of IDs of Servers attached to this Network | getServers(): array | setServers(array servers): void |
| `subnets` | [`Subnet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/subnet.md) | Required | Array subnets allocated in this Network | getSubnets(): array | setSubnets(array subnets): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\NetworkBuilder;
use HetznerCloudAPILib\ApiHelper;
use HetznerCloudAPILib\Models\Builders\Protection11Builder;
use HetznerCloudAPILib\Models\Builders\RouteBuilder;
use HetznerCloudAPILib\Models\Builders\SubnetBuilder;
use HetznerCloudAPILib\Models\Type42Enum;

$network = NetworkBuilder::init(
    '2016-01-30T23:50:00+00:00',
    4711,
    '10.0.0.0/16',
    ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'),
    'mynet',
    Protection11Builder::init(
        false
    )->build(),
    [
        RouteBuilder::init(
            '10.100.1.0/24',
            '10.0.1.1'
        )->build()
    ],
    [
        42
    ],
    [
        SubnetBuilder::init(
            '10.0.0.1',
            'eu-central',
            Type42Enum::CLOUD
        )
            ->ipRange('10.0.1.0/24')
            ->build()
    ]
)
    ->loadBalancers(
        [
            42
        ]
    )
    ->build();
```



