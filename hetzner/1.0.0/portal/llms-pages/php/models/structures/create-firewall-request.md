# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applyTo` | [`?(ApplyTo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation | getApplyTo(): ?array | setApplyTo(?array applyTo): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the Firewall | getName(): string | setName(string name): void |
| `rules` | [`?(Rule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/rule.md) | Optional | Array of rules | getRules(): ?array | setRules(?array rules): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateFirewallRequestBuilder;
use HetznerCloudAPILib\Models\Builders\ApplyToBuilder;
use HetznerCloudAPILib\Models\Type7Enum;
use HetznerCloudAPILib\Models\Builders\LabelSelector1Builder;
use HetznerCloudAPILib\Models\Builders\Server2Builder;
use HetznerCloudAPILib\ApiHelper;
use HetznerCloudAPILib\Models\Builders\RuleBuilder;
use HetznerCloudAPILib\Models\DirectionEnum;
use HetznerCloudAPILib\Models\ProtocolEnum;

$createFirewallRequest = CreateFirewallRequestBuilder::init(
    'Corporate Intranet Protection'
)
    ->applyTo(
        [
            ApplyToBuilder::init(
                Type7Enum::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )->build()
                )->build(),
            ApplyToBuilder::init(
                Type7Enum::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )->build()
                )->build(),
            ApplyToBuilder::init(
                Type7Enum::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )->build()
                )->build()
        ]
    )
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->rules(
        [
            RuleBuilder::init(
                DirectionEnum::IN,
                ProtocolEnum::TCP
            )
                ->description('description2')
                ->destinationIps(
                    [
                        'destination_ips1',
                        'destination_ips2',
                        'destination_ips3'
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
    ->build();
```



