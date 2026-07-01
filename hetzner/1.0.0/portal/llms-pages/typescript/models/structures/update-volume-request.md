# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Interface Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | [`Labels2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `name` | `string` | Required | New Volume name |


# Example

```ts
import { UpdateVolumeRequest } from 'hetzner-cloud-apilib';

const updateVolumeRequest: UpdateVolumeRequest = {
  name: 'database-storage',
  labels: {
    labelkey: 'labelkey4',
  },
};
```



