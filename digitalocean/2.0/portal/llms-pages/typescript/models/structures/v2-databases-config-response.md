# V2 Databases Config Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesConfigResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `config` | [`V2DatabasesConfigResponseConfig`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/oneof-anyof-definitions/v2-databases-config-response-config.md) | Required | This is a container for any-of cases. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  InternalTmpMemStorageEngine,
  V2DatabasesConfigResponse,
} from 'digitalocean-apilib';

const v2DatabasesConfigResponse: V2DatabasesConfigResponse = {
  config: {
    backupHour: 3,
    backupMinute: 30,
    binlogRetentionPeriod: 600,
    connectTimeout: 10,
    defaultTimeZone: '+03:00',
    groupConcatMaxLen: 1024,
    informationSchemaStatsExpiry: 86400,
    innodbFtMinTokenSize: 3,
    innodbFtServerStopwordTable: 'db_name/table_name',
    innodbLockWaitTimeout: 50,
    innodbLogBufferSize: 16777216,
    innodbOnlineAlterLogMaxSize: 134217728,
    innodbPrintAllDeadlocks: true,
    innodbRollbackOnTimeout: true,
    interactiveTimeout: 3600,
    internalTmpMemStorageEngine: InternalTmpMemStorageEngine.TempTable,
    longQueryTime: 10,
    maxAllowedPacket: 67108864,
    maxHeapTableSize: 16777216,
    netReadTimeout: 30,
    netWriteTimeout: 30,
    slowQueryLog: true,
    sortBufferSize: 262144,
    sqlMode: 'ANSI,TRADITIONAL',
    sqlRequirePrimaryKey: true,
    tmpTableSize: 16777216,
    waitTimeout: 28800,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



