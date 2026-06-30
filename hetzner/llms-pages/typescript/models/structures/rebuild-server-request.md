# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Interface Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `string` | Required | ID or name of Image to rebuilt from. |


# Example

```ts
import { RebuildServerRequest } from 'hetzner-cloud-apilib';

const rebuildServerRequest: RebuildServerRequest = {
  image: 'ubuntu-20.04',
};
```



