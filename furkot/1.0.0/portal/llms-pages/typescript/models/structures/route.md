# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type unknown.*


# Interface Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `bigint \| undefined` | Optional | route distance in meters |
| `duration` | `bigint \| undefined` | Optional | route duration in seconds |
| `mode` | [`Mode \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/typescript/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `string \| undefined` | Optional | route path compatible with Google polyline encoding algorithm |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Mode, Route } from 'furkot-tripslib';

const route: Route = {
  distance: BigInt(134),
  duration: BigInt(168),
  mode: Mode.Car,
  polyline: 'polyline0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



