# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw


# Interface Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelSelector` | [`LabelSelector5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `type` | [`Type7Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-7.md) | Optional | Type of the resource |


# Example

```ts
import { FirewallApplyToResources, Type7Enum } from 'hetzner-cloud-apilib';

const firewallApplyToResources: FirewallApplyToResources = {
  labelSelector: {
    selector: 'selector8',
  },
  server: {
    id: 14,
  },
  type: Type7Enum.Server,
};
```



