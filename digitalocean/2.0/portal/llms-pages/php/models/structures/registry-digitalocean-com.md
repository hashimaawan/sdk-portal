# Registry Digitalocean Com

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlZ2lzdHJ5RGlnaXRhbG9jZWFuQ29t

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`RegistryDigitaloceanCom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `auth` | `?string` | Optional | A base64 encoded string containing credentials for the container registry. | getAuth(): ?string | setAuth(?string auth): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\RegistryDigitaloceanComBuilder;
use DigitalOceanApiLib\ApiHelper;

$registryDigitaloceanCom = RegistryDigitaloceanComBuilder::init()
    ->auth('YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODI6YjdkMDNhNjk0N2IyMTdlZmI2ZjNlYzNiZDM1MDQ1ODIK')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



