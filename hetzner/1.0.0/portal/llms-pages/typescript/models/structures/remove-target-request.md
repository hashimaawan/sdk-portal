# Remove Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlbW92ZVRhcmdldFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`RemoveTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | [`Ip \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `labelSelector` | [`LabelSelector12 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `server` | [`Server16 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-29.md) | Required | Type of the resource |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { RemoveTargetRequest, Type29 } from 'hetzner-cloud-apilib';

const removeTargetRequest: RemoveTargetRequest = {
  type: Type29.Ip,
  ip: {
    ip: 'ip8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  labelSelector: {
    selector: 'selector8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  server: {
    id: 217.74,
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



