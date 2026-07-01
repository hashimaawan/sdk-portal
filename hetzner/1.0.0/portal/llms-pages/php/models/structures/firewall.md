# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type array.*


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
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
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

$firewall = FirewallBuilder::init(
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
            'key0' => 'labels2',
            'key1' => 'labels1'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



