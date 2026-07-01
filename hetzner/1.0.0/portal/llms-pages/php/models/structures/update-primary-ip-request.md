# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoDelete` | `?bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted | getAutoDelete(): ?bool | setAutoDelete(?bool autoDelete): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New unique name to set | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\UpdatePrimaryIpRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$updatePrimaryIpRequest = UpdatePrimaryIpRequestBuilder::init()
    ->autoDelete(true)
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-ip')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



