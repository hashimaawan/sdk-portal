# Server Backup

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlckJhY2t1cA

Will increase base Server costs by specific percentage

*This model accepts additional fields of type array.*


# Class Name

`ServerBackup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `percentage` | `string` | Required | Percentage by how much the base price will increase | getPercentage(): string | setPercentage(string percentage): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServerBackupBuilder;
use HetznerCloudApiLib\ApiHelper;

$serverBackup = ServerBackupBuilder::init(
    '20.0000000000'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



