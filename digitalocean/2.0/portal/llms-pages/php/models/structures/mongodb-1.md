# Mongodb 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk1vbmdvZGIx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Mongodb1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `endOfAvailability` | `?string` | Optional | A timestamp referring to the date when the particular version will no longer be available for creating new clusters. If null, the version does not have an end of availability timeline. | getEndOfAvailability(): ?string | setEndOfAvailability(?string endOfAvailability): void |
| `endOfLife` | `?string` | Optional | A timestamp referring to the date when the particular version will no longer be supported. If null, the version does not have an end of life timeline. | getEndOfLife(): ?string | setEndOfLife(?string endOfLife): void |
| `version` | `?string` | Optional | The engine version. | getVersion(): ?string | setVersion(?string version): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Mongodb1Builder;
use DigitalOceanApiLib\ApiHelper;

$mongodb1 = Mongodb1Builder::init()
    ->endOfAvailability('2023-05-09T00:00:00Z')
    ->endOfLife('2023-11-09T00:00:00Z')
    ->version('8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



