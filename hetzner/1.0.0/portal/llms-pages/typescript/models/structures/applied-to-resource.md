# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Interface Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server.md) | Optional | - |
| `type` | [`Type5Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-5.md) | Optional | Type of resource referenced |


# Example

```ts
import { AppliedToResource, Type5Enum } from 'hetzner-cloud-apilib';

const appliedToResource: AppliedToResource = {
  server: {
    id: 14,
  },
  type: Type5Enum.Server,
};
```



