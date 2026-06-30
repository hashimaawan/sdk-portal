# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q


# Interface Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `boolean \| undefined` | Optional | Auto-mount the Volume after attaching it |
| `server` | `number` | Required | ID of the Server the Volume will be attached to |


# Example

```ts
import { AttachVolumeRequest } from 'hetzner-cloud-apilib';

const attachVolumeRequest: AttachVolumeRequest = {
  server: 43,
  automount: false,
};
```



