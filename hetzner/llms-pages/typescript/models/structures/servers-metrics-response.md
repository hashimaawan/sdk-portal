# Servers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyME1ldHJpY3MlMjUyMFJlc3BvbnNl


# Interface Name

`ServersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/metrics.md) | Required | - |


# Example

```ts
import { ServersMetricsResponse } from 'hetzner-cloud-apilib';

const serversMetricsResponse: ServersMetricsResponse = {
  metrics: {
    end: '2017-01-01T23:00:00+00:00',
    start: '2017-01-01T00:00:00+00:00',
    step: 60,
    timeSeries: {
      'name_of_timeseries': {
        values: [
          null,
          null
        ],
      }
    },
  },
};
```



