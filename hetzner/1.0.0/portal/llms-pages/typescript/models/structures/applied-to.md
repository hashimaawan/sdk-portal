# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Interface Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `appliedToResources` | [`AppliedToResource[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/applied-to-resource.md) | Optional | - |
| `labelSelector` | [`LabelSelector \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector.md) | Optional | - |
| `server` | [`Server \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server.md) | Optional | - |
| `type` | [`Type6Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-6.md) | Required | Type of resource referenced |


# Example

```ts
import { AppliedTo, Type5Enum, Type6Enum } from 'hetzner-cloud-apilib';

const appliedTo: AppliedTo = {
  type: Type6Enum.Server,
  appliedToResources: [
    {
      server: {
        id: 14,
      },
      type: Type5Enum.Server,
    },
    {
      server: {
        id: 14,
      },
      type: Type5Enum.Server,
    }
  ],
  labelSelector: {
    selector: 'selector8',
  },
  server: {
    id: 14,
  },
};
```



