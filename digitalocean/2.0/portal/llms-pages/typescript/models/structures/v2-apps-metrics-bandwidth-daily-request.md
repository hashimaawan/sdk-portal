# V2 Apps Metrics Bandwidth Daily Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsMetricsBandwidthDailyRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appIds` | `string[]` | Required | A list of app IDs to query bandwidth metrics for.<br><br>**Constraints**: *Maximum Items*: `100` |
| `date` | `string \| undefined` | Optional | Optional day to query. Only the date component of the timestamp will be considered. Default: yesterday. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsMetricsBandwidthDailyRequest } from 'digitalocean-apilib';

const v2AppsMetricsBandwidthDailyRequest: V2AppsMetricsBandwidthDailyRequest = {
  appIds: [
    '4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf',
    'c2a93513-8d9b-4223-9d61-5e7272c81cf5'
  ],
  date: '2023-01-17T00:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



