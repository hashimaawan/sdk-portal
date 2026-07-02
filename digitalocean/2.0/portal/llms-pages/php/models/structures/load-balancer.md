# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional | The ID of a resource associated with a Kubernetes cluster. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | The name of a resource associated with a Kubernetes cluster. | getName(): ?string | setName(?string name): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\LoadBalancerBuilder;
use DigitalOceanApiLib\ApiHelper;

$loadBalancer = LoadBalancerBuilder::init()
    ->id('edb0478d-7436-11ea-86e6-0a58ac144b91')
    ->name('volume-001')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



