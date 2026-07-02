# Check

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkNoZWNr

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Check`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?string` | Optional, Read-only | A unique ID that can be used to identify and reference the check. | getId(): ?string | setId(?string id): void |
| `enabled` | `?bool` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` | getEnabled(): ?bool | setEnabled(?bool enabled): void |
| `name` | `?string` | Optional | A human-friendly display name. | getName(): ?string | setName(?string name): void |
| `regions` | [`?(string(Region8)[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. | getRegions(): ?array | setRegions(?array regions): void |
| `target` | `?string` | Optional | The endpoint to perform healthchecks on. | getTarget(): ?string | setTarget(?string target): void |
| `type` | [`?string(Type19)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-19.md) | Optional | The type of health check to perform. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\CheckBuilder;
use DigitalOceanApiLib\Models\Region8;
use DigitalOceanApiLib\Models\Type19;
use DigitalOceanApiLib\ApiHelper;

$check = CheckBuilder::init()
    ->id('5a4981aa-9653-4bd1-bef5-d6bff52042e4')
    ->enabled(true)
    ->name('Landing page check')
    ->regions(
        [
            Region8::US_EAST,
            Region8::EU_WEST
        ]
    )
    ->target('https://www.landingpage.com')
    ->type(Type19::HTTPS)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



