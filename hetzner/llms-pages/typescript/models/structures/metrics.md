# Metrics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRk1ldHJpY3M


# Interface Name

`Metrics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `end` | `string` | Required | End of period of metrics reported (in ISO-8601 format) |
| `start` | `string` | Required | Start of period of metrics reported (in ISO-8601 format) |
| `step` | `number` | Required | Resolution of results in seconds. |
| `timeSeries` | [`Record<string, TimeSeries>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/time-series.md) | Required | Hash with timeseries information, containing the name of timeseries as key |


# Example

```ts
import { Metrics } from 'hetzner-cloud-apilib';

const metrics: Metrics = {
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
};
```



