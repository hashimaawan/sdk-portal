# Load Balancer Service

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclNlcnZpY2U

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancerService`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `destinationPort` | `int` | Required | Port the Load Balancer will balance to | getDestinationPort(): int | setDestinationPort(int destinationPort): void |
| `healthCheck` | [`LoadBalancerServiceHealthCheck`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-service-health-check.md) | Required | Service health check | getHealthCheck(): LoadBalancerServiceHealthCheck | setHealthCheck(LoadBalancerServiceHealthCheck healthCheck): void |
| `http` | [`?LoadBalancerServiceHttp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-service-http.md) | Optional | Configuration option for protocols http and https | getHttp(): ?LoadBalancerServiceHttp | setHttp(?LoadBalancerServiceHttp http): void |
| `listenPort` | `int` | Required | Port the Load Balancer listens on | getListenPort(): int | setListenPort(int listenPort): void |
| `protocol` | [`string(Protocol7)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/protocol-7.md) | Required | Protocol of the Load Balancer | getProtocol(): string | setProtocol(string protocol): void |
| `proxyprotocol` | `bool` | Required | Is Proxyprotocol enabled or not | getProxyprotocol(): bool | setProxyprotocol(bool proxyprotocol): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceBuilder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceHealthCheckBuilder;
use HetznerCloudApiLib\Models\Protocol6;
use HetznerCloudApiLib\Models\Builders\HttpBuilder;
use HetznerCloudApiLib\Models\Protocol7;
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceHttpBuilder;
use HetznerCloudApiLib\ApiHelper;

$loadBalancerService = LoadBalancerServiceBuilder::init(
    80,
    LoadBalancerServiceHealthCheckBuilder::init(
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
        ->build(),
    443,
    Protocol7::HTTPS,
    false
)
    ->http(
        LoadBalancerServiceHttpBuilder::init()
            ->certificates(
                [
                    180
                ]
            )
            ->cookieLifetime(160)
            ->cookieName('cookie_name6')
            ->redirectHttp(false)
            ->stickySessions(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



