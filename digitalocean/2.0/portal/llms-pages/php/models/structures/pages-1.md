# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Pages1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `first` | `?string` | Optional | URI of the first page of the results. | getFirst(): ?string | setFirst(?string first): void |
| `prev` | `?string` | Optional | URI of the previous page of the results. | getPrev(): ?string | setPrev(?string prev): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Pages1Builder;
use DigitalOceanApiLib\ApiHelper;

$pages1 = Pages1Builder::init()
    ->first('https://api.digitalocean.com/v2/images?page=1')
    ->prev('https://api.digitalocean.com/v2/images?page=1')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



