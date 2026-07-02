# Inbound Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkluYm91bmRSdWxl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`InboundRule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ports` | `string` | Required | The ports on which traffic will be allowed specified as a string containing a single port, a range (e.g. "8000-9000"), or "0" when all ports are open for a protocol. For ICMP rules this parameter will always return "0". | getPorts(): string | setPorts(string ports): void |
| `protocol` | [`string(Protocol)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/protocol.md) | Required | The type of traffic to be allowed. This may be one of `tcp`, `udp`, or `icmp`. | getProtocol(): string | setProtocol(string protocol): void |
| `sources` | [`Sources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/sources.md) | Required | - | getSources(): Sources | setSources(Sources sources): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\InboundRuleBuilder;
use DigitalOceanApiLib\Models\Protocol;
use DigitalOceanApiLib\Models\Builders\SourcesBuilder;
use DigitalOceanApiLib\ApiHelper;

$inboundRule = InboundRuleBuilder::init(
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
    ->build();
```



