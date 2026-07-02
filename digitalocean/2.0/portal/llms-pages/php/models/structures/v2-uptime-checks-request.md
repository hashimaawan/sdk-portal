# V2 Uptime Checks Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2UptimeChecksRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `?bool` | Optional | A boolean value indicating whether the check is enabled/disabled.<br><br>**Default**: `true` | getEnabled(): ?bool | setEnabled(?bool enabled): void |
| `name` | `?string` | Optional | A human-friendly display name. | getName(): ?string | setName(?string name): void |
| `regions` | [`?(string(Region8)[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-8.md) | Optional | An array containing the selected regions to perform healthchecks from. | getRegions(): ?array | setRegions(?array regions): void |
| `target` | `?string` | Optional | The endpoint to perform healthchecks on. | getTarget(): ?string | setTarget(?string target): void |
| `type` | [`?string(Type19)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-19.md) | Optional | The type of health check to perform. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2UptimeChecksRequestBuilder;
use DigitalOceanApiLib\Models\Region8;
use DigitalOceanApiLib\Models\Type19;
use DigitalOceanApiLib\ApiHelper;

$v2UptimeChecksRequest = V2UptimeChecksRequestBuilder::init()
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



