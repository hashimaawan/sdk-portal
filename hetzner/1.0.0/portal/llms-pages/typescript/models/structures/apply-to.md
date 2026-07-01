# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGx5VG8

*This model accepts additional fields of type unknown.*


# Interface Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelSelector` | [`LabelSelector1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` |
| `server` | [`Server2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-7.md) | Required | Type of the resource |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ApplyTo, Type7 } from 'hetzner-cloud-apilib';

const applyTo: ApplyTo = {
  type: Type7.Server,
  labelSelector: {
    selector: 'selector8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  server: {
    id: 14,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



