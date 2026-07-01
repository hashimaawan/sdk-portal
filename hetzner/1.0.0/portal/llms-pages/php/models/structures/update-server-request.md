# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New name to set | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdateServerRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$updateServerRequest = UpdateServerRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-server')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



