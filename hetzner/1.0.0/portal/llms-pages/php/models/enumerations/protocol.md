# Protocol

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlByb3RvY29s

Type of traffic to allow


# Enum Type Name

`ProtocolEnum`


# Fields

| Name |
|  --- |
| `TCP` |
| `UDP` |
| `ICMP` |
| `ESP` |
| `GRE` |


# Example

```php
use HetznerCloudAPILib\Models\ProtocolEnum;

$protocol = ProtocolEnum::ESP;
```



