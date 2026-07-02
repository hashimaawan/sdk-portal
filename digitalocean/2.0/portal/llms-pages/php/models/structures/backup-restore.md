# Backup Restore

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkJhY2t1cFJlc3RvcmU

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`BackupRestore`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `backupCreatedAt` | `?DateTime` | Optional | The timestamp of an existing database cluster backup in ISO8601 combined date and time format. The most recent backup will be used if excluded. | getBackupCreatedAt(): ?\DateTime | setBackupCreatedAt(?\DateTime backupCreatedAt): void |
| `databaseName` | `string` | Required | The name of an existing database cluster from which the backup will be restored. | getDatabaseName(): string | setDatabaseName(string databaseName): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\BackupRestoreBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$backupRestore = BackupRestoreBuilder::init(
    'backend'
)
    ->backupCreatedAt(DateTimeHelper::fromRfc3339DateTime('2019-01-31T19:25:22Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



