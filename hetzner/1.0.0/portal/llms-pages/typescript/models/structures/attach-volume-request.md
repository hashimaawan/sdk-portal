# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `boolean \| undefined` | Optional | Auto-mount the Volume after attaching it |
| `server` | `number` | Required | ID of the Server the Volume will be attached to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AttachVolumeRequest } from 'hetzner-cloud-apilib';

const attachVolumeRequest: AttachVolumeRequest = {
  server: 43,
  automount: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



