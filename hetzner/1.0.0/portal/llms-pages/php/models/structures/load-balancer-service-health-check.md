# Load Balancer Service Health Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2VIZWFsdGhDaGVjaw

Service health check


# Class Name

`LoadBalancerServiceHealthCheck`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `http` | [`?Http`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/http.md) | Optional | Additional configuration for protocol http | getHttp(): ?Http | setHttp(?Http http): void |
| `interval` | `int` | Required | Time interval in seconds health checks are performed | getInterval(): int | setInterval(int interval): void |
| `port` | `int` | Required | Port the health check will be performed on | getPort(): int | setPort(int port): void |
| `protocol` | [`string(Protocol6)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/protocol-6.md) | Required | Type of the health check | getProtocol(): string | setProtocol(string protocol): void |
| `retries` | `int` | Required | Unsuccessful retries needed until a target is considered unhealthy; an unhealthy target needs the same number of successful retries to become healthy again | getRetries(): int | setRetries(int retries): void |
| `timeout` | `int` | Required | Time in seconds after an attempt is considered a timeout | getTimeout(): int | setTimeout(int timeout): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceHealthCheckBuilder;
use HetznerCloudApiLib\Models\Protocol6;
use HetznerCloudApiLib\Models\Builders\HttpBuilder;

$loadBalancerServiceHealthCheck = LoadBalancerServiceHealthCheckBuilder::init(
    15,
    4711,
    Protocol6::HTTP,
    3,
    10
)
    ->http(
        HttpBuilder::init(
            'path2'
        )
            ->domain('domain4')
            ->response('response8')
            ->statusCodes(
                [
                    'status_codes0',
                    'status_codes1',
                    'status_codes2'
                ]
            )
            ->tls(false)
            ->build()
    )
    ->build();
```



