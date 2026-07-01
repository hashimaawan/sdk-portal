# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`


# Class Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelSelector5Builder;

$labelSelector5 = LabelSelector5Builder::init(
    'env=prod'
)->build();
```



