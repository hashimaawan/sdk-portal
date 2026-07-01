# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type array.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`?(Action[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getActions(): ?array | setActions(?array actions): void |
| `firewall` | [`?Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall.md) | Optional | - | getFirewall(): ?Firewall | setFirewall(?Firewall firewall): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateFirewallResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;
use HetznerCloudApiLib\Models\Builders\FirewallBuilder;
use HetznerCloudApiLib\Models\Builders\AppliedToBuilder;
use HetznerCloudApiLib\Models\Type6;
use HetznerCloudApiLib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudApiLib\Models\Builders\ServerBuilder;
use HetznerCloudApiLib\Models\Type5;
use HetznerCloudApiLib\Models\Builders\LabelSelectorBuilder;
use HetznerCloudApiLib\Models\Builders\RuleBuilder;
use HetznerCloudApiLib\Models\Direction;
use HetznerCloudApiLib\Models\Protocol;

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
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ],
                '2016-01-30T23:55:00+00:00',
                Status::SUCCESS
            )
                ->error(
                    ErrorBuilder::init(
                        'action_failed',
                        'Action failed'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->finished('2016-01-30T23:56:00+00:00')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ActionBuilder::init(
                'apply_firewall',
                14,
                100,
                [
                    Resource2Builder::init(
                        42,
                        'server'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    Resource2Builder::init(
                        38,
                        'firewall'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                ],
                '2016-01-30T23:55:00+00:00',
                Status::SUCCESS
            )
                ->error(
                    ErrorBuilder::init(
                        'action_failed',
                        'Action failed'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->finished('2016-01-30T23:56:00+00:00')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->firewall(
        FirewallBuilder::init(
            [
                AppliedToBuilder::init(
                    Type6::SERVER
                )
                    ->appliedToResources(
                        [
                            AppliedToResourceBuilder::init()
                                ->server(
                                    ServerBuilder::init(
                                        14
                                    )
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                )
                                ->type(Type5::SERVER)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->labelSelector(
                        LabelSelectorBuilder::init(
                            'selector8'
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->server(
                        ServerBuilder::init(
                            14
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                AppliedToBuilder::init(
                    Type6::SERVER
                )
                    ->appliedToResources(
                        [
                            AppliedToResourceBuilder::init()
                                ->server(
                                    ServerBuilder::init(
                                        14
                                    )
                                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                        ->build()
                                )
                                ->type(Type5::SERVER)
                                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                ->build()
                        ]
                    )
                    ->labelSelector(
                        LabelSelectorBuilder::init(
                            'selector8'
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->server(
                        ServerBuilder::init(
                            14
                        )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            'created6',
            4,
            'name6',
            [
                RuleBuilder::init(
                    Direction::IN,
                    Protocol::UDP
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
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->labels(
                [
                    'key0' => 'labels2',
                    'key1' => 'labels1'
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



