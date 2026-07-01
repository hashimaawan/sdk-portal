# Change DNSPTR Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNoYW5nZUROU1BUUlJlcXVlc3Q


# Class Name

`ChangeDNSPTRRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Required | Hostname to set as a reverse DNS PTR entry, will reset to original default value if `null` | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `string` | Required | IP address for which to set the reverse DNS entry | getIp(): string | setIp(string ip): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ChangeDNSPTRRequestBuilder;

$changeDNSPTRRequest = ChangeDNSPTRRequestBuilder::init(
    '1.2.3.4'
)
    ->dnsPtr('server02.example.com')
    ->build();
```



