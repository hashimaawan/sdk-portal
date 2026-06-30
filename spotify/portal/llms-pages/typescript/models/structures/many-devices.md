# Many Devices

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRk1hbnlEZXZpY2Vz

*This model accepts additional fields of type unknown.*


# Interface Name

`ManyDevices`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `devices` | [`DeviceObject[]`](https://github.com/hashimaawan/sdk-portal/tree/main/spotify/llms-pages/typescript/models/structures/device-object.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ManyDevices,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const manyDevices: ManyDevices = {
  devices: [
    {
      id: 'id4',
      isActive: false,
      isPrivateSession: false,
      isRestricted: false,
      name: 'Kitchen speaker',
      type: 'computer',
      volumePercent: 59,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



