# V2 Databases Config Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMENvbmZpZyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DatabasesConfigRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `config` | [`V2DatabasesConfigRequestConfig \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/oneof-anyof-definitions/v2-databases-config-request-config.md) | Optional | This is a container for any-of cases. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2DatabasesConfigRequest } from 'digitalocean-apilib';

const v2DatabasesConfigRequest: V2DatabasesConfigRequest = {
  config: {
    backupHour: 23,
    backupMinute: 59,
    binlogRetentionPeriod: 600,
    connectTimeout: 196,
    defaultTimeZone: 'default_time_zone8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



