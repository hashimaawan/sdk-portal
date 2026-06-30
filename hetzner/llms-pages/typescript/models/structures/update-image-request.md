# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Interface Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | New description of Image |
| `labels` | `unknown \| undefined` | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type24Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |


# Example

```ts
import { Type24Enum, UpdateImageRequest } from 'hetzner-cloud-apilib';

const updateImageRequest: UpdateImageRequest = {
  description: 'My new Image description',
  labels: { 'labelkey': 'value' },
  type: Type24Enum.Snapshot,
};
```



