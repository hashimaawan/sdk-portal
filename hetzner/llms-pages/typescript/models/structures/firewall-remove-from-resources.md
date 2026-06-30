# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw


# Interface Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelSelector` | [`LabelSelector5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `type` | [`Type7Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```ts
import { FirewallRemoveFromResources, Type7Enum } from 'hetzner-cloud-apilib';

const firewallRemoveFromResources: FirewallRemoveFromResources = {
  labelSelector: {
    selector: 'selector8',
  },
  server: {
    id: 14,
  },
  type: Type7Enum.Server,
};
```



