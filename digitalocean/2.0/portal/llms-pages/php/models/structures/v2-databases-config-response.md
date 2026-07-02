# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `config` | [Config](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config.md)\|[Config](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config.md)1\|[Config](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/config.md)2 | Required | This is a container for any-of cases. | getConfig(): | setConfig( config): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesConfigResponseBuilder;
use DigitalOceanApiLib\Models\Builders\ConfigBuilder;
use DigitalOceanApiLib\Models\InternalTmpMemStorageEngine;
use DigitalOceanApiLib\ApiHelper;

$v2DatabasesConfigResponse = V2DatabasesConfigResponseBuilder::init(
    ConfigBuilder::init()
        ->backupHour(3)
        ->backupMinute(30)
        ->binlogRetentionPeriod(600)
        ->connectTimeout(10)
        ->defaultTimeZone('+03:00')
        ->groupConcatMaxLen(1024)
        ->informationSchemaStatsExpiry(86400)
        ->innodbFtMinTokenSize(3)
        ->innodbFtServerStopwordTable('db_name/table_name')
        ->innodbLockWaitTimeout(50)
        ->innodbLogBufferSize(16777216)
        ->innodbOnlineAlterLogMaxSize(134217728)
        ->innodbPrintAllDeadlocks(true)
        ->innodbRollbackOnTimeout(true)
        ->interactiveTimeout(3600)
        ->internalTmpMemStorageEngine(InternalTmpMemStorageEngine::TEMPTABLE)
        ->longQueryTime(10)
        ->maxAllowedPacket(67108864)
        ->maxHeapTableSize(16777216)
        ->netReadTimeout(30)
        ->netWriteTimeout(30)
        ->slowQueryLog(true)
        ->sortBufferSize(262144)
        ->sqlMode('ANSI,TRADITIONAL')
        ->sqlRequirePrimaryKey(true)
        ->tmpTableSize(16777216)
        ->waitTimeout(28800)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



