# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkFwcGx5VG8


# Interface Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelSelector` | [`LabelSelector1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `server` | [`Server2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type7Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-7.md) | Required | Type of the resource |


# Example

```ts
import { ApplyTo, Type7Enum } from 'hetzner-cloud-apilib';

const applyTo: ApplyTo = {
  type: Type7Enum.Server,
  labelSelector: {
    selector: 'selector8',
  },
  server: {
    id: 14,
  },
};
```



