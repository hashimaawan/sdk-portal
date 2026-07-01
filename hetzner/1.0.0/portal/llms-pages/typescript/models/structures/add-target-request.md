# Add Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFkZFRhcmdldFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`AddTargetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | [`Ip \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. |
| `labelSelector` | [`LabelSelector12 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` |
| `server` | [`Server16 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` |
| `type` | [`Type29`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-29.md) | Required | Type of the resource |
| `usePrivateIp` | `boolean \| undefined` | Optional | Use the private network IP instead of the public IP of the Server, requires the Server and Load Balancer to be in the same network. Default value is false. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AddTargetRequest, Type29 } from 'hetzner-cloud-apilib';

const addTargetRequest: AddTargetRequest = {
  type: Type29.Server,
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
  usePrivateIp: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



