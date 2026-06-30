# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `int` | Required | ID of the Server the Image was created from | getId(): int | setId(int id): void |
| `name` | `string` | Required | Server name at the time the Image was created | getName(): string | setName(string name): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\CreatedFromBuilder;

$createdFrom = CreatedFromBuilder::init(
    1,
    'Server'
)->build();
```



