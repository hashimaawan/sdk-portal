# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aliasIps` | `?(string[])` | Optional | Additional IPs to be assigned to this Server | getAliasIps(): ?array | setAliasIps(?array aliasIps): void |
| `ip` | `?string` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address | getIp(): ?string | setIp(?string ip): void |
| `network` | `int` | Required | ID of an existing network to attach the Server to | getNetwork(): int | setNetwork(int network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AttachToNetworkRequestBuilder;

$attachToNetworkRequest = AttachToNetworkRequestBuilder::init(
    4711
)
    ->aliasIps(
        [
            '10.0.1.2'
        ]
    )
    ->ip('10.0.1.1')
    ->build();
```



