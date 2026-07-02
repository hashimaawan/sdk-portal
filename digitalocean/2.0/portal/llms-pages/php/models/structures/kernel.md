# Kernel

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRktlcm5lbA

**Note**: All Droplets created after March 2017 use internal kernels by default.
These Droplets will have this attribute set to `null`.

The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)
for Droplets with externally managed kernels. This will initially be set to
the kernel of the base image when the Droplet is created.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Kernel`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | A unique number used to identify and reference a specific kernel. | getId(): ?int | setId(?int id): void |
| `name` | `?string` | Optional | The display name of the kernel. This is shown in the web UI and is generally a descriptive title for the kernel in question. | getName(): ?string | setName(?string name): void |
| `version` | `?string` | Optional | A standard kernel version string representing the version, patch, and release information. | getVersion(): ?string | setVersion(?string version): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\KernelBuilder;
use DigitalOceanApiLib\ApiHelper;

$kernel = KernelBuilder::init()
    ->id(7515)
    ->name('DigitalOcean GrubLoader v0.2 (20160714)')
    ->version('2016.07.13-DigitalOcean_loader_Ubuntu')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



