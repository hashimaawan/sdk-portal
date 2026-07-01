# Load Balancers Metrics Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwTWV0cmljcyUyNTIwUmVzcG9uc2U


# Interface Name

`LoadBalancersMetricsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `metrics` | [`Metrics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/metrics.md) | Required | - |


# Example

```ts
import { LoadBalancersMetricsResponse } from 'hetzner-cloud-apilib';

const loadBalancersMetricsResponse: LoadBalancersMetricsResponse = {
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



