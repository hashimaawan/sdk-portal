# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelSelectorBuilder;

$labelSelector = LabelSelectorBuilder::init(
    'env=prod'
)->build();
```



