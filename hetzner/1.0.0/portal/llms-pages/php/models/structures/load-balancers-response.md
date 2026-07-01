# Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancers` | [`LoadBalancer[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/load-balancer.md) | Required | - | getLoadBalancers(): array | setLoadBalancers(array loadBalancers): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LoadBalancersResponseBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerBuilder;
use HetznerCloudAPILib\Models\Builders\AlgorithmBuilder;
use HetznerCloudAPILib\Models\Type28Enum;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTypeBuilder;
use HetznerCloudAPILib\Models\Builders\PriceBuilder;
use HetznerCloudAPILib\Models\Builders\PriceHourlyBuilder;
use HetznerCloudAPILib\Models\Builders\PriceMonthlyBuilder;
use HetznerCloudAPILib\Models\Builders\LocationBuilder;
use HetznerCloudAPILib\Models\Builders\PrivateNetBuilder;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Builders\PublicNetBuilder;
use HetznerCloudAPILib\Models\Builders\Ipv4Builder;
use HetznerCloudAPILib\Models\Builders\Ipv6Builder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceHealthCheckBuilder;
use HetznerCloudAPILib\Models\Protocol6Enum;
use HetznerCloudAPILib\Models\Builders\HttpBuilder;
use HetznerCloudAPILib\Models\Protocol7Enum;
use HetznerCloudAPILib\Models\Builders\LoadBalancerServiceHTTPBuilder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTargetBuilder;
use HetznerCloudAPILib\Models\Type29Enum;
use HetznerCloudAPILib\Models\Builders\HealthStatusBuilder;
use HetznerCloudAPILib\Models\Status30Enum;
use HetznerCloudAPILib\Models\Builders\IpBuilder;
use HetznerCloudAPILib\Models\Builders\LabelSelector7Builder;
use HetznerCloudAPILib\Models\Builders\LoadBalancerTargetServerBuilder;
use HetznerCloudAPILib\Models\Builders\TargetBuilder;
use HetznerCloudAPILib\Models\Builders\Server11Builder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$loadBalancersResponse = LoadBalancersResponseBuilder::init(
    [
        LoadBalancerBuilder::init(
            AlgorithmBuilder::init(
                Type28Enum::ROUND_ROBIN
            )->build(),
            '2016-01-30T23:55:00+00:00',
            42,
            10000,
            [
                'key0' => 'labels8',
                'key1' => 'labels7',
                'key2' => 'labels6'
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
                        )->build(),
                        PriceMonthlyBuilder::init(
                            '1.1900000000000000',
                            '1.0000000000'
                        )->build()
                    )->build()
                ]
            )
                ->deprecated('2016-01-30T23:50:00+00:00')
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
            )->build(),
            'my-resource',
            [
                PrivateNetBuilder::init()
                    ->ip('10.0.0.2')
                    ->network(4711)
                    ->build()
            ],
            ProtectionBuilder::init(
                false
            )->build(),
            PublicNetBuilder::init(
                false,
                Ipv4Builder::init()
                    ->dnsPtr('lb1.example.com')
                    ->ip('1.2.3.4')
                    ->build(),
                Ipv6Builder::init()
                    ->dnsPtr('lb1.example.com')
                    ->ip('2001:db8::1')
                    ->build()
            )->build(),
            [
                LoadBalancerServiceBuilder::init(
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
                    ->build()
            ],
            [
                LoadBalancerTargetBuilder::init(
                    Type29Enum::IP
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
                    ->build()
            ]
        )
            ->ingoingTraffic(204)
            ->outgoingTraffic(30)
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->build()
        )->build()
    )->build();
```



