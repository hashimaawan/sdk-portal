# Update Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`UpdateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | New Description to set | getDescription(): ?string | setDescription(?string description): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New unique name to set | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdateFloatingIpRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$updateFloatingIpRequest = UpdateFloatingIpRequestBuilder::init()
    ->description('Web Frontend')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('Web Frontend')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



