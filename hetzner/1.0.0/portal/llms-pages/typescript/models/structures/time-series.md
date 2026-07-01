# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type unknown.*


# Interface Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `values` | [`TimeSeriesValues[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/oneof-anyof-definitions/time-series-values.md) | Required | This is 2d Array of a container for one-of cases. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { TimeSeries } from 'hetzner-cloud-apilib';

const timeSeries: TimeSeries = {
  values: [
    null,
    null
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



