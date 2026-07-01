# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)


# Class Name

`Labels2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelkey` | `?string` | Optional | - | getLabelkey(): ?string | setLabelkey(?string labelkey): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Labels2Builder;

$labels2 = Labels2Builder::init()
    ->labelkey('value')
    ->build();
```



