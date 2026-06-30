# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/typescript/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Interface Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `distance` | `bigint \| undefined` | Optional | route distance in meters |
| `duration` | `bigint \| undefined` | Optional | route duration in seconds |
| `mode` | [`ModeEnum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/typescript/models/enumerations/mode.md) | Optional | travel mode |
| `polyline` | `string \| undefined` | Optional | route path compatible with Google polyline encoding algorithm |


# Example

```ts
import { ModeEnum, Route } from 'furkot-tripslib';

const route: Route = {
  distance: BigInt(134),
  duration: BigInt(168),
  mode: ModeEnum.Car,
  polyline: 'polyline0',
};
```



