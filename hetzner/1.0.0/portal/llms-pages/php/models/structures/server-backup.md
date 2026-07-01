# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `percentage` | `string` | Required | Percentage by how much the base price will increase | getPercentage(): string | setPercentage(string percentage): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServerBackupBuilder;

$serverBackup = ServerBackupBuilder::init(
    '20.0000000000'
)->build();
```



