# App Bandwidth Usage

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkFwcEJhbmR3aWR0aFVzYWdl

Bandwidth usage for an app.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AppBandwidthUsage`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appId` | `?string` | Optional | The ID of the app. | getAppId(): ?string | setAppId(?string appId): void |
| `bandwidthBytes` | `?string` | Optional | The used bandwidth amount in bytes. | getBandwidthBytes(): ?string | setBandwidthBytes(?string bandwidthBytes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AppBandwidthUsageBuilder;
use DigitalOceanApiLib\ApiHelper;

$appBandwidthUsage = AppBandwidthUsageBuilder::init()
    ->appId('4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf')
    ->bandwidthBytes('513668')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



