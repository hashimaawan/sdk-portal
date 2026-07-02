# Region

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlZ2lvbg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Region`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `available` | `bool` | Required | This is a boolean value that represents whether new Droplets can be created in this region. | getAvailable(): bool | setAvailable(bool available): void |
| `features` | `string[]` | Required | This attribute is set to an array which contains features available in this region | getFeatures(): array | setFeatures(array features): void |
| `name` | `string` | Required | The display name of the region.  This will be a full name that is used in the control panel and other interfaces. | getName(): string | setName(string name): void |
| `sizes` | `string[]` | Required | This attribute is set to an array which contains the identifying slugs for the sizes available in this region. | getSizes(): array | setSizes(array sizes): void |
| `slug` | `string` | Required | A human-readable string that is used as a unique identifier for each region. | getSlug(): string | setSlug(string slug): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;

$region = RegionBuilder::init(
    true,
    [
        'private_networking',
        'backups',
        'ipv6',
        'metadata',
        'install_agent',
        'storage',
        'image_transfer'
    ],
    'New York 3',
    [
        's-1vcpu-1gb',
        's-1vcpu-2gb',
        's-1vcpu-3gb',
        's-2vcpu-2gb',
        's-3vcpu-1gb',
        's-2vcpu-4gb',
        's-4vcpu-8gb',
        's-6vcpu-16gb',
        's-8vcpu-32gb',
        's-12vcpu-48gb',
        's-16vcpu-64gb',
        's-20vcpu-96gb',
        's-24vcpu-128gb',
        's-32vcpu-192g'
    ],
    'nyc3'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



