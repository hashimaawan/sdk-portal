# V2 Monitoring Metrics Droplet Bandwidth Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBNb25pdG9yaW5nJTI1MjBNZXRyaWNzJTI1MjBEcm9wbGV0JTI1MjBCYW5kd2lkdGglMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2MonitoringMetricsDropletBandwidthResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Data`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/data.md) | Required | - |
| `status` | [`Status13`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-13.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Status13,
  V2MonitoringMetricsDropletBandwidthResponse,
} from 'digitalocean-apilib';

const v2MonitoringMetricsDropletBandwidthResponse: V2MonitoringMetricsDropletBandwidthResponse = {
  data: {
    result: [
      {
        metric: {
          'host_id': '19201920'
        },
        values: [
          null,
          null
        ],
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    resultType: 'matrix',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  status: Status13.Success,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



