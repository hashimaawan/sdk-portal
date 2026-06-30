# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `string` | Required | Primary IP address for which the reverse DNS entry should be set | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsChangeDnsPtrRequestBuilder;

$serversActionsChangeDnsPtrRequest = ServersActionsChangeDnsPtrRequestBuilder::init(
    '1.2.3.4'
)
    ->dnsPtr('server01.example.com')
    ->build();
```



