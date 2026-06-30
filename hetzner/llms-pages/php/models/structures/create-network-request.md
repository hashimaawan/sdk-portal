# Create Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNyZWF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`CreateNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of the whole network which must span all included subnets. Must be one of the private IPv4 ranges of RFC1918. Minimum network size is /24. We highly recommend that you pick a larger network with a /16 netmask. | getIpRange(): string | setIpRange(string ipRange): void |
| `labels` | [`?Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) | getLabels(): ?Labels | setLabels(?Labels labels): void |
| `name` | `string` | Required | Name of the network | getName(): string | setName(string name): void |
| `routes` | [`?(Route[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/route.md) | Optional | Array of routes set in this network. The destination of the route must be one of the private IPv4 ranges of RFC1918. The gateway must be a subnet/IP of the ip_range of the network object. The destination must not overlap with an existing ip_range in any subnets or with any destinations in other routes or with the first IP of the networks ip_range or with 172.31.1.1. The gateway cannot be the first IP of the networks ip_range and also cannot be 172.31.1.1. | getRoutes(): ?array | setRoutes(?array routes): void |
| `subnets` | [`?(Subnet1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/subnet-1.md) | Optional | Array of subnets allocated. | getSubnets(): ?array | setSubnets(?array subnets): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateNetworkRequestBuilder;
use HetznerCloudAPILib\Models\Builders\LabelsBuilder;
use HetznerCloudAPILib\Models\Builders\RouteBuilder;
use HetznerCloudAPILib\Models\Builders\Subnet1Builder;
use HetznerCloudAPILib\Models\Type42Enum;

$createNetworkRequest = CreateNetworkRequestBuilder::init(
    '10.0.0.0/16',
    'mynet'
)
    ->labels(
        LabelsBuilder::init()
            ->labelkey('labelkey4')
            ->build()
    )
    ->routes(
        [
            RouteBuilder::init(
                'destination8',
                'gateway6'
            )->build()
        ]
    )
    ->subnets(
        [
            Subnet1Builder::init(
                'network_zone2',
                Type42Enum::CLOUD
            )
                ->ipRange('ip_range6')
                ->build(),
            Subnet1Builder::init(
                'network_zone2',
                Type42Enum::CLOUD
            )
                ->ipRange('ip_range6')
                ->build(),
            Subnet1Builder::init(
                'network_zone2',
                Type42Enum::CLOUD
            )
                ->ipRange('ip_range6')
                ->build()
        ]
    )
    ->build();
```



