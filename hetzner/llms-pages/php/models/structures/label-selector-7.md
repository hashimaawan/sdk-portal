# Label Selector 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I3

Label selector and a list of selected targets


# Class Name

`LabelSelector7`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector | getSelector(): string | setSelector(string selector): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\LabelSelector7Builder;

$labelSelector7 = LabelSelector7Builder::init(
    'env=prod'
)->build();
```



