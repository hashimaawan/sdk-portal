# Load Balancers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Uy

*This model accepts additional fields of type array.*


# Class Name

`LoadBalancersResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer.md) | Required | - | getLoadBalancer(): LoadBalancer | setLoadBalancer(LoadBalancer loadBalancer): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\LoadBalancersResponse2Builder;
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

$loadBalancersResponse2 = LoadBalancersResponse2Builder::init(
    LoadBalancerBuilder::init(
        AlgorithmBuilder::init(
            Type28::ROUND_ROBIN
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build(),
        '2016-01-30T23:55:00+00:00',
        42,
        10000,
        [
            'key0' => 'labels2',
            'key1' => 'labels1'
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
        ->ingoingTraffic(216)
        ->outgoingTraffic(42)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



