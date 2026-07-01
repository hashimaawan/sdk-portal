# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA


# Class Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `serverType` | `string` | Required | ID or name of Server type the Server should migrate to | getServerType(): string | setServerType(string serverType): void |
| `upgradeDisk` | `bool` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) | getUpgradeDisk(): bool | setUpgradeDisk(bool upgradeDisk): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsChangeTypeRequestBuilder;

$serversActionsChangeTypeRequest = ServersActionsChangeTypeRequestBuilder::init(
    'cx11',
    true
)->build();
```



