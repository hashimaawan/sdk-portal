# Device Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkRldmljZU9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`DeviceObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| null \| undefined` | Optional | The device ID. This ID is unique and persistent to some extent. However, this is not guaranteed and any cached `device_id` should periodically be cleared out and refetched as necessary. |
| `isActive` | `boolean \| undefined` | Optional | If this device is the currently active device. |
| `isPrivateSession` | `boolean \| undefined` | Optional | If this device is currently in a private session. |
| `isRestricted` | `boolean \| undefined` | Optional | Whether controlling this device is restricted. At present if this is "true" then no Web API commands will be accepted by this device. |
| `name` | `string \| undefined` | Optional | A human-readable name for the device. Some devices have a name that the user can configure (e.g. \"Loudest speaker\") and some devices have a generic name associated with the manufacturer or device model. |
| `type` | `string \| undefined` | Optional | Device type, such as "computer", "smartphone" or "speaker". |
| `volumePercent` | `number \| null \| undefined` | Optional | The current volume in percent.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `supportsVolume` | `boolean \| undefined` | Optional | If this device can be used to set the volume. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  DeviceObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const deviceObject: DeviceObject = {
  id: 'id0',
  isActive: false,
  isPrivateSession: false,
  isRestricted: false,
  name: 'Kitchen speaker',
  type: 'computer',
  volumePercent: 59,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



