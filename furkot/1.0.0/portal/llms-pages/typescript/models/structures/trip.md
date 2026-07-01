# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlRyaXA


# Interface Name

`Trip`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `begin` | `string \| undefined` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `description` | `string \| undefined` | Optional | description of the trip (truncated to 200 characters) |
| `end` | `string \| undefined` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm |
| `id` | `string \| undefined` | Optional | Unique ID of the trip |
| `name` | `string \| undefined` | Optional | name of the trip |


# Example

```ts
import { Trip } from 'furkot-tripslib';

const trip: Trip = {
  begin: '2016-03-13T12:52:32.123Z',
  description: 'description8',
  end: '2016-03-13T12:52:32.123Z',
  id: 'id8',
  name: 'name8',
};
```



