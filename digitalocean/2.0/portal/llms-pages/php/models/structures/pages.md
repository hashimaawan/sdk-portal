# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Pages`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `last` | `?string` | Optional | URI of the last page of the results. | getLast(): ?string | setLast(?string last): void |
| `next` | `?string` | Optional | URI of the next page of the results. | getNext(): ?string | setNext(?string next): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PagesBuilder;
use DigitalOceanApiLib\ApiHelper;

$pages = PagesBuilder::init()
    ->last('https://api.digitalocean.com/v2/images?page=2')
    ->next('https://api.digitalocean.com/v2/images?page=2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



