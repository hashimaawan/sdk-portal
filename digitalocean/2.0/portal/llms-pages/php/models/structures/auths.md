# Auths

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkF1dGhz

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Auths`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `registryDigitaloceanCom` | [`?RegistryDigitaloceanCom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/registry-digitalocean-com.md) | Optional | - | getRegistryDigitaloceanCom(): ?RegistryDigitaloceanCom | setRegistryDigitaloceanCom(?RegistryDigitaloceanCom registryDigitaloceanCom): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AuthsBuilder;
use DigitalOceanApiLib\Models\Builders\RegistryDigitaloceanComBuilder;
use DigitalOceanApiLib\ApiHelper;

$auths = AuthsBuilder::init()
    ->registryDigitaloceanCom(
        RegistryDigitaloceanComBuilder::init()
            ->auth('auth0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



