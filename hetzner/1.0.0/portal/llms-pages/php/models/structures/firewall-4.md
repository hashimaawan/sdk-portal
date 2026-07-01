# Firewall 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsNA


# Class Name

`Firewall4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `firewall` | `?int` | Optional | ID of the Firewall | getFirewall(): ?int | setFirewall(?int firewall): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\Firewall4Builder;

$firewall4 = Firewall4Builder::init()
    ->firewall(176)
    ->build();
```



