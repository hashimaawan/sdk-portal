# Change Loadbalancer Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkNoYW5nZUxvYWRiYWxhbmNlckRuc1B0clJlcXVlc3Q


# Class Name

`ChangeLoadbalancerDnsPtrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Required | Hostname to set as a reverse DNS PTR entry | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `string` | Required | Public IP address for which the reverse DNS entry should be set | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeLoadbalancerDnsPtrRequestBuilder;

$changeLoadbalancerDnsPtrRequest = ChangeLoadbalancerDnsPtrRequestBuilder::init(
    '1.2.3.4'
)
    ->dnsPtr('lb1.example.com')
    ->build();
```



