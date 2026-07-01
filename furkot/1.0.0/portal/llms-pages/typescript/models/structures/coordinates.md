# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type unknown.*


# Interface Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lat` | `number \| undefined` | Optional | latitude |
| `lon` | `number \| undefined` | Optional | longitude |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Coordinates } from 'furkot-tripslib';

const coordinates: Coordinates = {
  lat: 182.98,
  lon: 16.08,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



