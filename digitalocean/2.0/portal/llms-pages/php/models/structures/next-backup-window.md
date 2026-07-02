# Next Backup Window

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk5leHRCYWNrdXBXaW5kb3c

The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`NextBackupWindow`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `end` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format specifying the end of the Droplet's backup window. | getEnd(): ?\DateTime | setEnd(?\DateTime end): void |
| `start` | `?DateTime` | Optional | A time value given in ISO8601 combined date and time format specifying the start of the Droplet's backup window. | getStart(): ?\DateTime | setStart(?\DateTime start): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\NextBackupWindowBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\ApiHelper;

$nextBackupWindow = NextBackupWindowBuilder::init()
    ->end(DateTimeHelper::fromRfc3339DateTime('2019-12-04T23:00:00Z'))
    ->start(DateTimeHelper::fromRfc3339DateTime('2019-12-04T00:00:00Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



