# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Interface Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the snapshot from being deleted |


# Example

```ts
import { ImagesActionsChangeProtectionRequest } from 'hetzner-cloud-apilib';

const imagesActionsChangeProtectionRequest: ImagesActionsChangeProtectionRequest = {
  mDelete: true,
};
```



