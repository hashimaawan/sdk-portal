# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewalls` | [`Firewall[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall.md) | Required | - | getFirewalls(): array | setFirewalls(array firewalls): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FirewallsResponseBuilder;
use HetznerCloudApiLib\Models\Builders\FirewallBuilder;
use HetznerCloudApiLib\Models\Builders\AppliedToBuilder;
use HetznerCloudApiLib\Models\Type6;
use HetznerCloudApiLib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudApiLib\Models\Builders\ServerBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Type5;
use HetznerCloudApiLib\Models\Builders\LabelSelectorBuilder;
use HetznerCloudApiLib\Models\Builders\RuleBuilder;
use HetznerCloudApiLib\Models\Direction;
use HetznerCloudApiLib\Models\Protocol;
use HetznerCloudApiLib\Models\Builders\MetaBuilder;
use HetznerCloudApiLib\Models\Builders\PaginationBuilder;

$firewallsResponse = FirewallsResponseBuilder::init(
    [
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
                    ->build()
            ],
            '2016-01-30T23:55:00+00:00',
            42,
            'my-resource',
            [
                RuleBuilder::init(
                    Direction::IN,
                    Protocol::UDP
                )
                    ->description('description2')
                    ->destinationIps(
                        [
                            '28.239.13.1/32',
                            '28.239.14.0/24',
                            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
                        ]
                    )
                    ->port('80')
                    ->sourceIps(
                        [
                            '28.239.13.1/32',
                            '28.239.14.0/24',
                            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->labels(
                [
                    'key0' => 'labels4',
                    'key1' => 'labels5'
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



