# Firewall 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsMQ

An object specifying allow and deny rules to control traffic to the load balancer.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Firewall1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allow` | `?(string[])` | Optional | the rules for allowing traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') | getAllow(): ?array | setAllow(?array allow): void |
| `deny` | `?(string[])` | Optional | the rules for denying traffic to the load balancer (in the form 'ip:1.2.3.4' or 'cidr:1.2.0.0/16') | getDeny(): ?array | setDeny(?array deny): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Firewall1Builder;
use DigitalOceanApiLib\ApiHelper;

$firewall1 = Firewall1Builder::init()
    ->allow(
        [
            'ip:1.2.3.4',
            'cidr:2.3.0.0/16'
        ]
    )
    ->deny(
        [
            'ip:1.2.3.4',
            'cidr:2.3.0.0/16'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



