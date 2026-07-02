# V2 Apps Metrics Bandwidth Daily Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBNZXRyaWNzJTI1MjBCYW5kd2lkdGglMjUyMERhaWx5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsMetricsBandwidthDailyResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appBandwidthUsage` | [`AppBandwidthUsage[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/app-bandwidth-usage.md) | Optional | A list of bandwidth usage details by app. |
| `date` | `string \| undefined` | Optional | The date for the metrics data. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2AppsMetricsBandwidthDailyResponse } from 'digitalocean-apilib';

const v2AppsMetricsBandwidthDailyResponse: V2AppsMetricsBandwidthDailyResponse = {
  appBandwidthUsage: [
    {
      appId: 'app_id4',
      bandwidthBytes: 'bandwidth_bytes6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      appId: 'app_id4',
      bandwidthBytes: 'bandwidth_bytes6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  date: '2023-01-17T00:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



