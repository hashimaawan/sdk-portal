# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | - | getDescription(): ?string | setDescription(?string description): void |
| `homeLocation` | `?string` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. | getHomeLocation(): ?string | setHomeLocation(?string homeLocation): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `server` | `?int` | Optional | Server to assign the Floating IP to | getServer(): ?int | setServer(?int server): void |
| `type` | [`string(Type17)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-17.md) | Required | Floating IP type | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\CreateFloatingIpRequestBuilder;
use HetznerCloudApiLib\Models\Type17;
use HetznerCloudApiLib\ApiHelper;

$createFloatingIpRequest = CreateFloatingIpRequestBuilder::init(
    Type17::IPV4
)
    ->description('Web Frontend')
    ->homeLocation('fsn1')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('Web Frontend')
    ->server(42)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



