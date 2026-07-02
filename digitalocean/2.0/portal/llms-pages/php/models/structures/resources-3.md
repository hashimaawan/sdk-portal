# Resources 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc291cmNlczM

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Resources3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceId` | `?string` | Optional | The identifier of a resource. | getResourceId(): ?string | setResourceId(?string resourceId): void |
| `resourceType` | [`?string(ResourceType2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/resource-type-2.md) | Optional | The type of the resource. | getResourceType(): ?string | setResourceType(?string resourceType): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Resources3Builder;
use DigitalOceanApiLib\Models\ResourceType2;
use DigitalOceanApiLib\ApiHelper;

$resources3 = Resources3Builder::init()
    ->resourceId('3d80cb72-342b-4aaa-b92e-4e4abb24a933')
    ->resourceType(ResourceType2::VOLUME)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



