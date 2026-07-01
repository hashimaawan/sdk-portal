# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | ID of the Resource | getId(): ?int | setId(?int id): void |
| `status` | [`?string(Status72Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server | getStatus(): ?string | setStatus(?string status): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudAPILib\Models\Status72Enum;

$serverPublicNetFirewall = ServerPublicNetFirewallBuilder::init()
    ->id(42)
    ->status(Status72Enum::APPLIED)
    ->build();
```



