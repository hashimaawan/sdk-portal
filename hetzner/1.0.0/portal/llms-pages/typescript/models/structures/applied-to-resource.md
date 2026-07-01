# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl

*This model accepts additional fields of type unknown.*


# Interface Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server.md) | Optional | - |
| `type` | [`Type5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-5.md) | Optional | Type of resource referenced |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AppliedToResource, Type5 } from 'hetzner-cloud-apilib';

const appliedToResource: AppliedToResource = {
  server: {
    id: 14,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  type: Type5.Server,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



