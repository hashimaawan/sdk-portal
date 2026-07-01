# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type63 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateImageRequest, Type63 } from 'hetzner-cloud-apilib';

const createImageRequest: CreateImageRequest = {
  description: 'my image',
  labels: {
    labelkey: 'labelkey4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  type: Type63.Snapshot,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



