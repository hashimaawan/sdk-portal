# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`?(Action[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getActions(): ?array | setActions(?array actions): void |
| `firewall` | [`?Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall.md) | Optional | - | getFirewall(): ?Firewall | setFirewall(?Firewall firewall): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateFirewallResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;
use HetznerCloudAPILib\Models\Builders\FirewallBuilder;
use HetznerCloudAPILib\Models\Builders\AppliedToBuilder;
use HetznerCloudAPILib\Models\Type6Enum;
use HetznerCloudAPILib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudAPILib\Models\Builders\ServerBuilder;
use HetznerCloudAPILib\Models\Type5Enum;
use HetznerCloudAPILib\Models\Builders\LabelSelectorBuilder;
use HetznerCloudAPILib\Models\Builders\RuleBuilder;
use HetznerCloudAPILib\Models\DirectionEnum;
use HetznerCloudAPILib\Models\ProtocolEnum;

$createFirewallResponse = CreateFirewallResponseBuilder::init()
    ->actions(
        [
            ActionBuilder::init(
                'set_firewall_rules',
                13,
                100,
                [
                    Resource2Builder::init(
                        38,
                        'firewall'
                    )->build()
                ],
                '2016-01-30T23:55:00+00:00',
                StatusEnum::SUCCESS
            )
                ->error(
                    ErrorBuilder::init(
                        'action_failed',
                        'Action failed'
                    )->build()
                )
                ->finished('2016-01-30T23:56:00+00:00')
                ->build(),
            ActionBuilder::init(
                'apply_firewall',
                14,
                100,
                [
                    Resource2Builder::init(
                        42,
                        'server'
                    )->build(),
                    Resource2Builder::init(
                        38,
                        'firewall'
                    )->build()
                ],
                '2016-01-30T23:55:00+00:00',
                StatusEnum::SUCCESS
            )
                ->error(
                    ErrorBuilder::init(
                        'action_failed',
                        'Action failed'
                    )->build()
                )
                ->finished('2016-01-30T23:56:00+00:00')
                ->build()
        ]
    )
    ->firewall(
        FirewallBuilder::init(
            [
                AppliedToBuilder::init(
                    Type6Enum::SERVER
                )
                    ->appliedToResources(
                        [
                            AppliedToResourceBuilder::init()
                                ->server(
                                    ServerBuilder::init(
                                        14
                                    )->build()
                                )
                                ->type(Type5Enum::SERVER)
                                ->build()
                        ]
                    )
                    ->labelSelector(
                        LabelSelectorBuilder::init(
                            'selector8'
                        )->build()
                    )
                    ->server(
                        ServerBuilder::init(
                            14
                        )->build()
                    )->build(),
                AppliedToBuilder::init(
                    Type6Enum::SERVER
                )
                    ->appliedToResources(
                        [
                            AppliedToResourceBuilder::init()
                                ->server(
                                    ServerBuilder::init(
                                        14
                                    )->build()
                                )
                                ->type(Type5Enum::SERVER)
                                ->build()
                        ]
                    )
                    ->labelSelector(
                        LabelSelectorBuilder::init(
                            'selector8'
                        )->build()
                    )
                    ->server(
                        ServerBuilder::init(
                            14
                        )->build()
                    )->build()
            ],
            'created6',
            4,
            'name6',
            [
                RuleBuilder::init(
                    DirectionEnum::IN,
                    ProtocolEnum::UDP
                )
                    ->description('description2')
                    ->destinationIps(
                        [
                            'destination_ips1',
                            'destination_ips2',
                            'destination_ips3'
                        ]
                    )
                    ->port('port8')
                    ->sourceIps(
                        [
                            'source_ips1',
                            'source_ips2',
                            'source_ips3'
                        ]
                    )
                    ->build()
            ]
        )
            ->labels(
                [
                    'key0' => 'labels2',
                    'key1' => 'labels1'
                ]
            )
            ->build()
    )
    ->build();
```



