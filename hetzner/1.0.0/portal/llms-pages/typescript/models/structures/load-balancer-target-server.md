# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerTargetServer } from 'hetzner-cloud-apilib';

const loadBalancerTargetServer: LoadBalancerTargetServer = {
  id: 80,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



