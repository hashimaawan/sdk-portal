# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Interface Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | Description of the Image, will be auto-generated if not set |
| `labels` | [`Labels \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `type` | [`Type63Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |


# Example

```ts
import { CreateImageRequest, Type63Enum } from 'hetzner-cloud-apilib';

const createImageRequest: CreateImageRequest = {
  description: 'my image',
  labels: {
    labelkey: 'labelkey4',
  },
  type: Type63Enum.Snapshot,
};
```



