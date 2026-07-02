# V2 Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancer` | [`?LoadBalancer1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/load-balancer-1.md) | Optional | - | getLoadBalancer(): ?LoadBalancer1 | setLoadBalancer(?LoadBalancer1 loadBalancer): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2LoadBalancersResponse1Builder;
use DigitalOceanApiLib\Models\Builders\LoadBalancer1Builder;
use DigitalOceanApiLib\Models\Builders\ForwardingRuleBuilder;
use DigitalOceanApiLib\Models\EntryProtocol;
use DigitalOceanApiLib\Models\TargetProtocol;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Algorithm;
use DigitalOceanApiLib\Utils\DateTimeHelper;

$v2LoadBalancersResponse1 = V2LoadBalancersResponse1Builder::init()
    ->loadBalancer(
        LoadBalancer1Builder::init(
            [
                ForwardingRuleBuilder::init(
                    220,
                    EntryProtocol::HTTP2,
                    104,
                    TargetProtocol::HTTPS
                )
                    ->certificateId('certificate_id4')
                    ->tlsPassthrough(false)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                ForwardingRuleBuilder::init(
                    220,
                    EntryProtocol::HTTP2,
                    104,
                    TargetProtocol::HTTPS
                )
                    ->certificateId('certificate_id4')
                    ->tlsPassthrough(false)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
            ->algorithm(Algorithm::ROUND_ROBIN)
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->disableLetsEncryptDnsRecords(false)
            ->enableBackendKeepalive(false)
            ->enableProxyProtocol(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



