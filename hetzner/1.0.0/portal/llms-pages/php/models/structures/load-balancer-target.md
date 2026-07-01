# Load Balancer Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldA


# Class Name

`LoadBalancerTarget`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `healthStatus` | [`?(HealthStatus[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/health-status.md) | Optional | List of health statuses of the services on this target | getHealthStatus(): ?array | setHealthStatus(?array healthStatus): void |
| `ip` | [`?Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. | getIp(): ?Ip | setIp(?Ip ip): void |
| `labelSelector` | [`?LabelSelector7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector-7.md) | Optional | Label selector and a list of selected targets | getLabelSelector(): ?LabelSelector7 | setLabelSelector(?LabelSelector7 labelSelector): void |
| `server` | [`?LoadBalancerTargetServer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-target-server.md) | Optional | Server where the traffic should be routed through | getServer(): ?LoadBalancerTargetServer | setServer(?LoadBalancerTargetServer server): void |
| `targets` | [`?(Target[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/target.md) | Optional | List of selected targets | getTargets(): ?array | setTargets(?array targets): void |
| `type` | [`string(Type29Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-29.md) | Required | Type of the resource | getType(): string | setType(string type): void |
| `usePrivateIp` | `?bool` | Optional | Use the private network IP instead of the public IP. Default value is false. | getUsePrivateIp(): ?bool | setUsePrivateIp(?bool usePrivateIp): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancerTargetBuilder;
use HetznerCloudAPILib\Models\Type29Enum;
use HetznerCloudAPILib\Models\Builders\HealthStatusBuilder;
use HetznerCloudAPILib\Models\Status30Enum;
use HetznerCloudAPILib\Models\Builders\IpBuilder;
use HetznerCloudAPILib\Models\Builders\LabelSelector7Builder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTargetServerBuilder;
use HetznerCloudAPILib\Models\Builders\TargetBuilder;
use HetznerCloudAPILib\Models\Builders\Server11Builder;

$loadBalancerTarget = LoadBalancerTargetBuilder::init(
    Type29Enum::LABEL_SELECTOR
)
    ->healthStatus(
        [
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30Enum::UNKNOWN)
                ->build(),
            HealthStatusBuilder::init()
                ->listenPort(142)
                ->status(Status30Enum::UNKNOWN)
                ->build()
        ]
    )
    ->ip(
        IpBuilder::init(
            'ip8'
        )->build()
    )
    ->labelSelector(
        LabelSelector7Builder::init(
            'selector8'
        )->build()
    )
    ->server(
        LoadBalancerTargetServerBuilder::init(
            14
        )->build()
    )
    ->targets(
        [
            TargetBuilder::init()
                ->healthStatus(
                    [
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build(),
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build()
                    ]
                )
                ->server(
                    Server11Builder::init(
                        14
                    )->build()
                )
                ->type('type2')
                ->usePrivateIp(false)
                ->build(),
            TargetBuilder::init()
                ->healthStatus(
                    [
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build(),
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build()
                    ]
                )
                ->server(
                    Server11Builder::init(
                        14
                    )->build()
                )
                ->type('type2')
                ->usePrivateIp(false)
                ->build(),
            TargetBuilder::init()
                ->healthStatus(
                    [
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build(),
                        HealthStatusBuilder::init()
                            ->listenPort(142)
                            ->status(Status30Enum::UNKNOWN)
                            ->build()
                    ]
                )
                ->server(
                    Server11Builder::init(
                        14
                    )->build()
                )
                ->type('type2')
                ->usePrivateIp(false)
                ->build()
        ]
    )
    ->build();
```



