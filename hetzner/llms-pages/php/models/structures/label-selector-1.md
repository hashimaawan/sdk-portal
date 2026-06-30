# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`


# Class Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelSelector1Builder;

$labelSelector1 = LabelSelector1Builder::init(
    'selector2'
)->build();
```



