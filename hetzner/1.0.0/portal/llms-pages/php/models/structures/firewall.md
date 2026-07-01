# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxs


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appliedTo` | [`AppliedTo[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/applied-to.md) | Required | - | getAppliedTo(): array | setAppliedTo(array appliedTo): void |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) | getCreated(): string | setCreated(string created): void |
| `id` | `int` | Required | ID of the Resource | getId(): int | setId(int id): void |
| `labels` | `?array<string,string>` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. | getName(): string | setName(string name): void |
| `rules` | [`Rule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/rule.md) | Required | - | getRules(): array | setRules(array rules): void |


# Example

```php
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

$firewall = FirewallBuilder::init(
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
            'key0' => 'labels2',
            'key1' => 'labels1'
        ]
    )
    ->build();
```



