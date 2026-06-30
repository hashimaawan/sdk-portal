# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options


# Class Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enableIpv4` | `?bool` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. | getEnableIpv4(): ?bool | setEnableIpv4(?bool enableIpv4): void |
| `enableIpv6` | `?bool` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. | getEnableIpv6(): ?bool | setEnableIpv6(?bool enableIpv6): void |
| `ipv4` | `?int` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. | getIpv4(): ?int | setIpv4(?int ipv4): void |
| `ipv6` | `?int` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. | getIpv6(): ?int | setIpv6(?int ipv6): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\PublicNet5Builder;

$publicNet5 = PublicNet5Builder::init()
    ->enableIpv4(false)
    ->enableIpv6(false)
    ->ipv4(42)
    ->ipv6(102)
    ->build();
```



