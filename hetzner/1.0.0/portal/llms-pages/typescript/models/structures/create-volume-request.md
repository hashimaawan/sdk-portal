# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `automount` | `boolean \| undefined` | Optional | Auto-mount Volume after attach. `server` must be provided. |
| `format` | `string \| undefined` | Optional | Format Volume after creation. One of: `xfs`, `ext4` |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `location` | `string \| undefined` | Optional | Location to create the Volume in (can be omitted if Server is specified) |
| `name` | `string` | Required | Name of the volume |
| `server` | `number \| undefined` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) |
| `size` | `number` | Required | Size of the Volume in GB |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateVolumeRequest } from 'hetzner-cloud-apilib';

const createVolumeRequest: CreateVolumeRequest = {
  name: 'databases-storage',
  size: 42,
  automount: false,
  format: 'xfs',
  labels: { 'labelkey': 'value' },
  location: 'nbg1',
  server: 182,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



