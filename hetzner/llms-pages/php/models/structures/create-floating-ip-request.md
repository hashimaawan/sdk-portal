# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | - | getDescription(): ?string | setDescription(?string description): void |
| `homeLocation` | `?string` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. | getHomeLocation(): ?string | setHomeLocation(?string homeLocation): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `server` | `?int` | Optional | Server to assign the Floating IP to | getServer(): ?int | setServer(?int server): void |
| `type` | [`string(Type17Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-17.md) | Required | Floating IP type | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreateFloatingIPRequestBuilder;
use HetznerCloudAPILib\Models\Type17Enum;
use HetznerCloudAPILib\ApiHelper;

$createFloatingIPRequest = CreateFloatingIPRequestBuilder::init(
    Type17Enum::IPV4
)
    ->description('Web Frontend')
    ->homeLocation('fsn1')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('Web Frontend')
    ->server(42)
    ->build();
```



