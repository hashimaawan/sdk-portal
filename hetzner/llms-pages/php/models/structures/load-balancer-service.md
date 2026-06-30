# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `destinationPort` | `int` | Required | Port the Load Balancer will balance to | getDestinationPort(): int | setDestinationPort(int destinationPort): void |
| `healthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/load-balancer-service-health-check.md) | Required | Service health check | getHealthCheck(): LoadBalancerServiceHealthCheck | setHealthCheck(LoadBalancerServiceHealthCheck healthCheck): void |
| `http` | [`?LoadBalancerServiceHTTP`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https | getHttp(): ?LoadBalancerServiceHTTP | setHttp(?LoadBalancerServiceHTTP http): void |
| `listenPort` | `int` | Required | Port the Load Balancer listens on | getListenPort(): int | setListenPort(int listenPort): void |
| `protocol` | [`string(Protocol7Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer | getProtocol(): string | setProtocol(string protocol): void |
| `proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not | getProxyprotocol(): bool | setProxyprotocol(bool proxyprotocol): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceHealthCheckBuilder;
use HetznerCloudAPILib\Models\Protocol6Enum;
use HetznerCloudAPILib\Models\Builders\HttpBuilder;
use HetznerCloudAPILib\Models\Protocol7Enum;
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceHTTPBuilder;

$loadBalancerService = LoadBalancerServiceBuilder::init(
    80,
    LoadBalancerServiceHealthCheckBuilder::init(
        15,
        4711,
        Protocol6Enum::HTTP,
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
        ->build(),
    443,
    Protocol7Enum::HTTPS,
    false
)
    ->http(
        LoadBalancerServiceHTTPBuilder::init()
            ->certificates(
                [
                    180
                ]
            )
            ->cookieLifetime(160)
            ->cookieName('cookie_name6')
            ->redirectHttp(false)
            ->stickySessions(false)
            ->build()
    )
    ->build();
```



