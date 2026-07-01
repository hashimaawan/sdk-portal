# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `dnsPtr` | `?string` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` | getDnsPtr(): ?string | setDnsPtr(?string dnsPtr): void |
| `ip` | `string` | Required | Primary IP address for which the reverse DNS entry should be set | getIp(): string | setIp(string ip): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsChangeDnsPtrRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$serversActionsChangeDnsPtrRequest = ServersActionsChangeDnsPtrRequestBuilder::init(
    '1.2.3.4'
)
    ->dnsPtr('server01.example.com')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



