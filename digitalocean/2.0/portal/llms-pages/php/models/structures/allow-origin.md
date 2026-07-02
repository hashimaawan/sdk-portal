# Allow Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFsbG93T3JpZ2lu

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AllowOrigin`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `exact` | `?string` | Optional | Exact string match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getExact(): ?string | setExact(?string exact): void |
| `prefix` | `?string` | Optional | Prefix-based match. Only 1 of `exact`, `prefix`, or `regex` must be set.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getPrefix(): ?string | setPrefix(?string prefix): void |
| `regex` | `?string` | Optional | RE2 style regex-based match. Only 1 of `exact`, `prefix`, or `regex` must be set. For more information about RE2 syntax, see: https://github.com/google/re2/wiki/Syntax<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getRegex(): ?string | setRegex(?string regex): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AllowOriginBuilder;
use DigitalOceanApiLib\ApiHelper;

$allowOrigin = AllowOriginBuilder::init()
    ->exact('https://www.example.com')
    ->prefix('https://www.example.com')
    ->regex('^.*example.com')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



