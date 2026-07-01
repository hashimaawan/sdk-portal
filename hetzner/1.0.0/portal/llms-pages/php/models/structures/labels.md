# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelkey` | `?string` | Optional | New label | getLabelkey(): ?string | setLabelkey(?string labelkey): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelsBuilder;

$labels = LabelsBuilder::init()
    ->labelkey('value')
    ->build();
```



