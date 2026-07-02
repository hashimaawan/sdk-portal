# Databases

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRhdGFiYXNlcw

Tagged Resource Statistics include metadata regarding the resource type that has been tagged.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Databases`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `count` | `?int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` | getCount(): ?int | setCount(?int count): void |
| `lastTaggedUri` | `?string` | Optional | The URI for the last tagged object for this type of resource. | getLastTaggedUri(): ?string | setLastTaggedUri(?string lastTaggedUri): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DatabasesBuilder;
use DigitalOceanApiLib\ApiHelper;

$databases = DatabasesBuilder::init()
    ->count(5)
    ->lastTaggedUri('https://api.digitalocean.com/v2/images/7555620')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



