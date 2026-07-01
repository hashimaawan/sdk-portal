# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Volume from being deleted |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { VolumesActionsChangeProtectionRequest } from 'hetzner-cloud-apilib';

const volumesActionsChangeProtectionRequest: VolumesActionsChangeProtectionRequest = {
  mDelete: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



