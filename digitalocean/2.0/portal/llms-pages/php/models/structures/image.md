# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `registry` | `?string` | Optional | The registry name. Must be left empty for the `DOCR` registry type. | getRegistry(): ?string | setRegistry(?string registry): void |
| `registryType` | [`?string(RegistryType)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/registry-type.md) | Optional | - DOCKER_HUB: The DockerHub container registry type.<br>- DOCR: The DigitalOcean container registry type. | getRegistryType(): ?string | setRegistryType(?string registryType): void |
| `repository` | `?string` | Optional | The repository name. | getRepository(): ?string | setRepository(?string repository): void |
| `tag` | `?string` | Optional | The repository tag. Defaults to `latest` if not provided.<br><br>**Default**: `'latest'` | getTag(): ?string | setTag(?string tag): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\ImageBuilder;
use DigitalOceanApiLib\Models\RegistryType;
use DigitalOceanApiLib\ApiHelper;

$image = ImageBuilder::init()
    ->registry('registry.hub.docker.com')
    ->registryType(RegistryType::DOCR)
    ->repository('origin/master')
    ->tag('latest')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



