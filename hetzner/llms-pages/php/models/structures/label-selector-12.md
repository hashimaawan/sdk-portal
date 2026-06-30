# Label Selector 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3IxMg

Configuration for label selector targets, required if type is `label_selector`


# Class Name

`LabelSelector12`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelSelector12Builder;

$labelSelector12 = LabelSelector12Builder::init(
    'env=prod'
)->build();
```



