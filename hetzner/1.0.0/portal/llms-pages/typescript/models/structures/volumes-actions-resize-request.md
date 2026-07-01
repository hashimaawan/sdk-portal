# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `number` | Required | New Volume size in GB (must be greater than current size) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { VolumesActionsResizeRequest } from 'hetzner-cloud-apilib';

const volumesActionsResizeRequest: VolumesActionsResizeRequest = {
  size: 50,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



