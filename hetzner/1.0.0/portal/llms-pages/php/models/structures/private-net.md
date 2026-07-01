# Private Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ


# Class Name

`PrivateNet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ip` | `?string` | Optional | - | getIp(): ?string | setIp(?string ip): void |
| `network` | `?int` | Optional | - | getNetwork(): ?int | setNetwork(?int network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrivateNetBuilder;

$privateNet = PrivateNetBuilder::init()
    ->ip('10.0.0.2')
    ->network(4711)
    ->build();
```



