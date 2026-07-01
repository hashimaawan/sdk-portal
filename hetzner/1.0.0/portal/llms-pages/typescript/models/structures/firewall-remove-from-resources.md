# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw

*This model accepts additional fields of type unknown.*


# Interface Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelSelector` | [`LabelSelector5 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` |
| `server` | [`Server9 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` |
| `type` | [`Type7 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-7.md) | Optional | Type of the resource |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { FirewallRemoveFromResources, Type7 } from 'hetzner-cloud-apilib';

const firewallRemoveFromResources: FirewallRemoveFromResources = {
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
  type: Type7.Server,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



