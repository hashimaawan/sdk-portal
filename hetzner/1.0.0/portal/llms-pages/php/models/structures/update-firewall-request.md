# Update Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`UpdateFirewallRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New Firewall name | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdateFirewallRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$updateFirewallRequest = UpdateFirewallRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('new-name')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



