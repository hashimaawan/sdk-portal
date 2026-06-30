# Private Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlByaXZhdGVOZXQ0


# Class Name

`PrivateNet4`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aliasIps` | `?(string[])` | Optional | - | getAliasIps(): ?array | setAliasIps(?array aliasIps): void |
| `ip` | `?string` | Optional | - | getIp(): ?string | setIp(?string ip): void |
| `macAddress` | `?string` | Optional | - | getMacAddress(): ?string | setMacAddress(?string macAddress): void |
| `network` | `?int` | Optional | - | getNetwork(): ?int | setNetwork(?int network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PrivateNet4Builder;

$privateNet4 = PrivateNet4Builder::init()
    ->aliasIps(
        [
            'alias_ips0',
            'alias_ips9'
        ]
    )
    ->ip('10.0.0.2')
    ->macAddress('86:00:ff:2a:7d:e1')
    ->network(4711)
    ->build();
```



