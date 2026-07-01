# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer | getAlgorithm(): Algorithm | setAlgorithm(Algorithm algorithm): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `includedTraffic` | `int` | Required | Free Traffic for the current billing period in bytes | getIncludedTraffic(): int | setIncludedTraffic(int includedTraffic): void |
| `ingoingTraffic` | `?int` | Required | Inbound Traffic for the current billing period in bytes | getIngoingTraffic(): ?int | setIngoingTraffic(?int ingoingTraffic): void |
| `labels` | `array<string,string>` | Required | User-defined labels (key-value pairs) | getLabels(): array | setLabels(array labels): void |
| `loadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-type.md) | Required | - | getLoadBalancerType(): LoadBalancerType | setLoadBalancerType(LoadBalancerType loadBalancerType): void |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/location.md) | Required | - | getLocation(): Location | setLocation(Location location): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `outgoingTraffic` | `?int` | Required | Outbound Traffic for the current billing period in bytes | getOutgoingTraffic(): ?int | setOutgoingTraffic(?int outgoingTraffic): void |
| `privateNet` | [`PrivateNet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/private-net.md) | Required | Private networks information | getPrivateNet(): array | setPrivateNet(array privateNet): void |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/protection.md) | Required | Protection configuration for the Resource | getProtection(): Protection | setProtection(Protection protection): void |
| `publicNet` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/public-net.md) | Required | Public network information | getPublicNet(): PublicNet | setPublicNet(PublicNet publicNet): void |
| `services` | [`LoadBalancerService[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer | getServices(): array | setServices(array services): void |
| `targets` | [`LoadBalancerTarget[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer | getTargets(): array | setTargets(array targets): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancerBuilder;
use HetznerCloudApiLib\Models\Builders\AlgorithmBuilder;
use HetznerCloudApiLib\Models\Type28;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudApiLib\Models\Builders\PriceBuilder;
use HetznerCloudApiLib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudApiLib\Models\Builders\PriceMonthlyBuilder;
use HetznerCloudApiLib\Models\Builders\LocationBuilder;
use HetznerCloudApiLib\Models\Builders\PrivateNetBuilder;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Builders\PublicNetBuilder;
use HetznerCloudApiLib\Models\Builders\Ipv4Builder;
use HetznerCloudApiLib\Models\Builders\Ipv6Builder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceBuilder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceHealthCheckBuilder;
use HetznerCloudApiLib\Models\Protocol6;
use HetznerCloudApiLib\Models\Builders\HttpBuilder;
use HetznerCloudApiLib\Models\Protocol7;
use HetznerCloudApiLib\Models\Builders\LoadBalancerServiceHttpBuilder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerTargetBuilder;
use HetznerCloudApiLib\Models\Type29;
use HetznerCloudApiLib\Models\Builders\HealthStatusBuilder;
use HetznerCloudApiLib\Models\Status30;
use HetznerCloudApiLib\Models\Builders\IpBuilder;
use HetznerCloudApiLib\Models\Builders\LabelSelector7Builder;
use HetznerCloudApiLib\Models\Builders\LoadBalancerTargetServerBuilder;
use HetznerCloudApiLib\Models\Builders\TargetBuilder;
use HetznerCloudApiLib\Models\Builders\Server11Builder;

$loadBalancer = LoadBalancerBuilder::init(
    AlgorithmBuilder::init(
        Type28::ROUND_ROBIN
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    '2016-01-30T23:55:00+00:00',
    42,
    10000,
    [
        'key0' => 'labels8',
        'key1' => 'labels7'
    ],
    LoadBalancerTypeBuilder::init(
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
        ->build(),
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
    'my-resource',
    [
        PrivateNetBuilder::init()
            ->ip('10.0.0.2')
            ->network(4711)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ],
    ProtectionBuilder::init(
        false
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    PublicNetBuilder::init(
        false,
        Ipv4Builder::init()
            ->dnsPtr('lb1.example.com')
            ->ip('1.2.3.4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        Ipv6Builder::init()
            ->dnsPtr('lb1.example.com')
            ->ip('2001:db8::1')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    [
        LoadBalancerServiceBuilder::init(
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
            ->build()
    ],
    [
        LoadBalancerTargetBuilder::init(
            Type29::IP
        )
            ->healthStatus(
                [
                    HealthStatusBuilder::init()
                        ->listenPort(142)
                        ->status(Status30::UNKNOWN)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    HealthStatusBuilder::init()
                        ->listenPort(142)
                        ->status(Status30::UNKNOWN)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->ip(
                IpBuilder::init(
                    'ip8'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->labelSelector(
                LabelSelector7Builder::init(
                    'selector8'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->server(
                LoadBalancerTargetServerBuilder::init(
                    14
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->targets(
                [
                    TargetBuilder::init()
                        ->healthStatus(
                            [
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build(),
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ]
                        )
                        ->server(
                            Server11Builder::init(
                                14
                            )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->type('type2')
                        ->usePrivateIp(false)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    TargetBuilder::init()
                        ->healthStatus(
                            [
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build(),
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ]
                        )
                        ->server(
                            Server11Builder::init(
                                14
                            )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->type('type2')
                        ->usePrivateIp(false)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    TargetBuilder::init()
                        ->healthStatus(
                            [
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build(),
                                HealthStatusBuilder::init()
                                    ->listenPort(142)
                                    ->status(Status30::UNKNOWN)
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            ]
                        )
                        ->server(
                            Server11Builder::init(
                                14
                            )
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        )
                        ->type('type2')
                        ->usePrivateIp(false)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->ingoingTraffic(210)
    ->outgoingTraffic(36)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



