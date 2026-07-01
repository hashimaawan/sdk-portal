# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | New description of Image |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type24 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Type24, UpdateImageRequest } from 'hetzner-cloud-apilib';

const updateImageRequest: UpdateImageRequest = {
  description: 'My new Image description',
  labels: { 'labelkey': 'value' },
  type: Type24.Snapshot,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



