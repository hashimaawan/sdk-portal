# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `cost` | `?string` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. | getCost(): ?string | setCost(?string cost): void |
| `id` | `?string` | Optional | The unique identifier for the resource associated with the Droplet. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The name of the resource associated with the Droplet. | getName(): ?string | setName(?string name): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\FloatingIpBuilder;
use DigitalOceanApiLib\ApiHelper;

$floatingIp = FloatingIpBuilder::init()
    ->cost('0.05')
    ->id('61486916')
    ->name('ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



