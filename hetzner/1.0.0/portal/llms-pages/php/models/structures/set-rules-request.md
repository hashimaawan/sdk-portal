# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rules` | [`Rule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` | getRules(): array | setRules(array rules): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\SetRulesRequestBuilder;
use HetznerCloudApiLib\Models\Builders\RuleBuilder;
use HetznerCloudApiLib\Models\Direction;
use HetznerCloudApiLib\Models\Protocol;
use HetznerCloudApiLib\ApiHelper;

$setRulesRequest = SetRulesRequestBuilder::init(
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
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



