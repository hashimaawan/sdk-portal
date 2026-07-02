# Scheduled Runs

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlNjaGVkdWxlZFJ1bnM

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ScheduledRuns`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lastRunAt` | `string \| null \| undefined` | Optional | Indicates last run time. null value indicates trigger not run yet. |
| `nextRunAt` | `string \| null \| undefined` | Optional | Indicates next run time. null value indicates trigger will not run. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ScheduledRuns } from 'digitalocean-apilib';

const scheduledRuns: ScheduledRuns = {
  lastRunAt: '2022-11-11T04:16:45Z',
  nextRunAt: '2022-11-11T04:16:45Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



