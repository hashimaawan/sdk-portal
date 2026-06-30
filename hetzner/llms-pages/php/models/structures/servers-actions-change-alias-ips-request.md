# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aliasIps` | `string[]` | Required | New alias IPs to set for this Server | getAliasIps(): array | setAliasIps(array aliasIps): void |
| `network` | `int` | Required | ID of an existing Network already attached to the Server | getNetwork(): int | setNetwork(int network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsChangeAliasIpsRequestBuilder;

$serversActionsChangeAliasIpsRequest = ServersActionsChangeAliasIpsRequestBuilder::init(
    [
        '10.0.1.2'
    ],
    4711
)->build();
```



