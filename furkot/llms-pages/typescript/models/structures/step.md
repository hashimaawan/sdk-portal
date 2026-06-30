# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/typescript/x-redirect/JTI0bSUyRlN0ZXA


# Interface Name

`Step`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address` | `string \| undefined` | Optional | address of the stop |
| `arrival` | `string \| undefined` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm |
| `coordinates` | [`Coordinates \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/typescript/models/structures/coordinates.md) | Optional | geographical coordinates of the stop |
| `departure` | `string \| undefined` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm |
| `name` | `string \| undefined` | Optional | name of the stop |
| `nights` | `bigint \| undefined` | Optional | number of nights |
| `passthru` | `boolean \| undefined` | Optional | true for pass-through points anchoring route |
| `route` | [`Route \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/typescript/models/structures/route.md) | Optional | route leading to the stop |
| `url` | `string \| undefined` | Optional | url of the page with more information about the stop |


# Example

```ts
import { Step } from 'furkot-tripslib';

const step: Step = {
  address: 'address4',
  arrival: '2016-03-13T12:52:32.123Z',
  coordinates: {
    lat: 182.98,
    lon: 16.08,
  },
  departure: '2016-03-13T12:52:32.123Z',
  name: 'name8',
};
```



