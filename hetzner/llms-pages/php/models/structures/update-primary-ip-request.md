# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q


# Class Name

`UpdatePrimaryIPRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `autoDelete` | `?bool` | Optional | Delete this Primary IP when the resource it is assigned to is deleted | getAutoDelete(): ?bool | setAutoDelete(?bool autoDelete): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New unique name to set | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdatePrimaryIPRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$updatePrimaryIPRequest = UpdatePrimaryIPRequestBuilder::init()
    ->autoDelete(true)
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-ip')
    ->build();
```



