# V2 Load Balancers Forwarding Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMEZvcndhcmRpbmclMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2LoadBalancersForwardingRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `forwardingRules` | [`ForwardingRule[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/forwarding-rule.md) | Required | **Constraints**: *Minimum Items*: `1` | getForwardingRules(): array | setForwardingRules(array forwardingRules): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2LoadBalancersForwardingRulesRequestBuilder;
use DigitalOceanApiLib\Models\Builders\ForwardingRuleBuilder;
use DigitalOceanApiLib\Models\EntryProtocol;
use DigitalOceanApiLib\Models\TargetProtocol;
use DigitalOceanApiLib\ApiHelper;

$v2LoadBalancersForwardingRulesRequest = V2LoadBalancersForwardingRulesRequestBuilder::init(
    [
        ForwardingRuleBuilder::init(
            443,
            EntryProtocol::HTTPS,
            80,
            TargetProtocol::HTTP
        )
            ->certificateId('892071a0-bb95-49bc-8021-3afd67a210bf')
            ->tlsPassthrough(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



