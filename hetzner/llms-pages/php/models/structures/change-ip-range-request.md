# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ipRange` | `string` | Required | The new prefix for the whole Network | getIpRange(): string | setIpRange(string ipRange): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeIPRangeRequestBuilder;

$changeIPRangeRequest = ChangeIPRangeRequestBuilder::init(
    '10.0.0.0/12'
)->build();
```



