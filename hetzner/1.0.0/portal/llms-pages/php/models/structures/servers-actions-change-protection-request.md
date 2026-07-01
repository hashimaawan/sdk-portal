# Servers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `delete` | `?bool` | Optional | If true, prevents the Server from being deleted (currently delete and rebuild attribute needs to have the same value) | getDelete(): ?bool | setDelete(?bool delete): void |
| `rebuild` | `?bool` | Optional | If true, prevents the Server from being rebuilt (currently delete and rebuild attribute needs to have the same value) | getRebuild(): ?bool | setRebuild(?bool rebuild): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsChangeProtectionRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$serversActionsChangeProtectionRequest = ServersActionsChangeProtectionRequestBuilder::init()
    ->delete(true)
    ->rebuild(true)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



