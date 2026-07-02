# V2 Databases Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMEZpcmV3YWxsJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesFirewallRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `rules` | [`?(Rule1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/rule-1.md) | Optional | - | getRules(): ?array | setRules(?array rules): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesFirewallRequestBuilder;
use DigitalOceanApiLib\Models\Builders\Rule1Builder;
use DigitalOceanApiLib\Models\Type7;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$v2DatabasesFirewallRequest = V2DatabasesFirewallRequestBuilder::init()
    ->rules(
        [
            Rule1Builder::init(
                Type7::IP_ADDR,
                'value0'
            )
                ->clusterUuid('cluster_uuid4')
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->uuid('uuid4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Rule1Builder::init(
                Type7::IP_ADDR,
                'value0'
            )
                ->clusterUuid('cluster_uuid4')
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->uuid('uuid4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



