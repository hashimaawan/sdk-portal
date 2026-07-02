# Action 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFjdGlvbjE

The linked actions can be used to check the status of a Droplet's create event.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Action1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `href` | `?string` | Optional | A URL that can be used to access the action. | getHref(): ?string | setHref(?string href): void |
| `id` | `?int` | Optional | A unique numeric ID that can be used to identify and reference an action. | getId(): ?int | setId(?int id): void |
| `rel` | `?string` | Optional | A string specifying the type of the related action. | getRel(): ?string | setRel(?string rel): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Action1Builder;
use DigitalOceanApiLib\ApiHelper;

$action1 = Action1Builder::init()
    ->href('https://api.digitalocean.com/v2/actions/7515')
    ->id(7515)
    ->rel('create')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



