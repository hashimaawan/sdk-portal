# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applyTo` | [`?(ApplyTo[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation | getApplyTo(): ?array | setApplyTo(?array applyTo): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `string` | Required | Name of the Firewall | getName(): string | setName(string name): void |
| `rules` | [`?(Rule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/rule.md) | Optional | Array of rules | getRules(): ?array | setRules(?array rules): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateFirewallRequestBuilder;
use HetznerCloudApiLib\Models\Builders\ApplyToBuilder;
use HetznerCloudApiLib\Models\Type7;
use HetznerCloudApiLib\Models\Builders\LabelSelector1Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Server2Builder;
use HetznerCloudApiLib\Models\Builders\RuleBuilder;
use HetznerCloudApiLib\Models\Direction;
use HetznerCloudApiLib\Models\Protocol;

$createFirewallRequest = CreateFirewallRequestBuilder::init(
    'Corporate Intranet Protection'
)
    ->applyTo(
        [
            ApplyToBuilder::init(
                Type7::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ApplyToBuilder::init(
                Type7::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ApplyToBuilder::init(
                Type7::SERVER
            )
                ->labelSelector(
                    LabelSelector1Builder::init(
                        'selector8'
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->server(
                    Server2Builder::init(
                        14
                    )
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->rules(
        [
            RuleBuilder::init(
                Direction::IN,
                Protocol::TCP
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
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



