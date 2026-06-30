# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | New description of Image | getDescription(): ?string | setDescription(?string description): void |
| `labels` | `?array` | Optional | User-defined labels (key-value pairs) | getLabels(): ?array | setLabels(?array labels): void |
| `type` | [`?string(Type24Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-24.md) | Optional | Destination Image type to convert to | getType(): ?string | setType(?string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\UpdateImageRequestBuilder;
use HetznerCloudAPILib\ApiHelper;
use HetznerCloudAPILib\Models\Type24Enum;

$updateImageRequest = UpdateImageRequestBuilder::init()
    ->description('My new Image description')
    ->labels(ApiHelper::deserialize('{"labelkey":"value"}'))
    ->type(Type24Enum::SNAPSHOT)
    ->build();
```



