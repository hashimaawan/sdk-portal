# State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRlMw

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`State3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `previousOutage` | [`PreviousOutage \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/previous-outage.md) | Optional | - |
| `regions` | [`Regions \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/regions.md) | Optional | A map of region to regional state |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { State3, Status16 } from 'digitalocean-apilib';

const state3: State3 = {
  previousOutage: {
    durationSeconds: 16,
    endedAt: 'ended_at4',
    region: 'region8',
    startedAt: 'started_at4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  regions: {
    euWest: {
      status: Status16.Down,
      statusChangedAt: 'status_changed_at4',
      thirtyDayUptimePercentage: 227.78,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    usEast: {
      status: Status16.Down,
      statusChangedAt: 'status_changed_at4',
      thirtyDayUptimePercentage: 121.56,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



