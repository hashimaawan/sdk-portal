# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewalls` | [`Firewall[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall.md) | Required | - | getFirewalls(): array | setFirewalls(array firewalls): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FirewallsResponseBuilder;
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
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$firewallsResponse = FirewallsResponseBuilder::init(
    [
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
                    )->build()
            ],
            '2016-01-30T23:55:00+00:00',
            42,
            'my-resource',
            [
                RuleBuilder::init(
                    DirectionEnum::IN,
                    ProtocolEnum::UDP
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
                    ->build()
            ]
        )
            ->labels(
                [
                    'key0' => 'labels4',
                    'key1' => 'labels5'
                ]
            )
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



