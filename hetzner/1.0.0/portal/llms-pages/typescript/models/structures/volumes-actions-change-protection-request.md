# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Interface Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Volume from being deleted |


# Example

```ts
import { VolumesActionsChangeProtectionRequest } from 'hetzner-cloud-apilib';

const volumesActionsChangeProtectionRequest: VolumesActionsChangeProtectionRequest = {
  mDelete: true,
};
```



