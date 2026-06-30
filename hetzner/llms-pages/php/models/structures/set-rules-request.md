# Set Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNldFJ1bGVzUmVxdWVzdA


# Class Name

`SetRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rules` | [`Rule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/rule.md) | Required | Array of rules<br><br>**Constraints**: *Maximum Items*: `50` | getRules(): array | setRules(array rules): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\SetRulesRequestBuilder;
use HetznerCloudAPILib\Models\Builders\RuleBuilder;
use HetznerCloudAPILib\Models\DirectionEnum;
use HetznerCloudAPILib\Models\ProtocolEnum;

$setRulesRequest = SetRulesRequestBuilder::init(
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
)->build();
```



