# Pending Change

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlBlbmRpbmdDaGFuZ2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`PendingChange`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dropletId` | `?int` | Optional | - | getDropletId(): ?int | setDropletId(?int dropletId): void |
| `removing` | `?bool` | Optional | - | getRemoving(): ?bool | setRemoving(?bool removing): void |
| `status` | `?string` | Optional | - | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\PendingChangeBuilder;
use DigitalOceanApiLib\ApiHelper;

$pendingChange = PendingChangeBuilder::init()
    ->dropletId(8043964)
    ->removing(false)
    ->status('waiting')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



