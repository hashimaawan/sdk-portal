# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | `string` | Required | ID or name of Image to rebuilt from. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { RebuildServerRequest } from 'hetzner-cloud-apilib';

const rebuildServerRequest: RebuildServerRequest = {
  image: 'ubuntu-20.04',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



