# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `inboundRules` | [`?(InboundRule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/inbound-rule.md) | Required | - | getInboundRules(): ?array | setInboundRules(?array inboundRules): void |
| `outboundRules` | [`?(OutboundRule[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/outbound-rule.md) | Required | - | getOutboundRules(): ?array | setOutboundRules(?array outboundRules): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2FirewallsRulesRequestBuilder;
use DigitalOceanApiLib\Models\Builders\InboundRuleBuilder;
use DigitalOceanApiLib\Models\Protocol;
use DigitalOceanApiLib\Models\Builders\SourcesBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\OutboundRuleBuilder;
use DigitalOceanApiLib\Models\Builders\DestinationsBuilder;

$v2FirewallsRulesRequest = V2FirewallsRulesRequestBuilder::init()
    ->inboundRules(
        [
            InboundRuleBuilder::init(
                '8000',
                Protocol::TCP,
                SourcesBuilder::init()
                    ->addresses(
                        [
                            '1.2.3.4',
                            '18.0.0.0/8'
                        ]
                    )
                    ->dropletIds(
                        [
                            8043964
                        ]
                    )
                    ->kubernetesIds(
                        [
                            '41b74c5d-9bd0-5555-5555-a57c495b81a3'
                        ]
                    )
                    ->loadBalancerUids(
                        [
                            '4de7ac8b-495b-4884-9a69-1050c6793cd6'
                        ]
                    )
                    ->tags(
                        [
                            'tags1',
                            'tags2',
                            'tags3'
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->outboundRules(
        [
            OutboundRuleBuilder::init(
                '8000',
                Protocol::TCP,
                DestinationsBuilder::init()
                    ->addresses(
                        [
                            '1.2.3.4',
                            '18.0.0.0/8'
                        ]
                    )
                    ->dropletIds(
                        [
                            8043964
                        ]
                    )
                    ->kubernetesIds(
                        [
                            '41b74c5d-9bd0-5555-5555-a57c495b81a3'
                        ]
                    )
                    ->loadBalancerUids(
                        [
                            '4de7ac8b-495b-4884-9a69-1050c6793cd6'
                        ]
                    )
                    ->tags(
                        [
                            'tags7',
                            'tags8',
                            'tags9'
                        ]
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



