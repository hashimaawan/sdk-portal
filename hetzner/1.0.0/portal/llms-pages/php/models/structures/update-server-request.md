# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `name` | `?string` | Optional | New name to set | getName(): ?string | setName(?string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdateServerRequestBuilder;
use HetznerCloudAPILib\ApiHelper;

$updateServerRequest = UpdateServerRequestBuilder::init()
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->name('my-server')
    ->build();
```



