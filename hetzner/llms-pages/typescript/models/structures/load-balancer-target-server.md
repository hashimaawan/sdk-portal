# Load Balancer Target Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclRhcmdldFNlcnZlcg

Server where the traffic should be routed through


# Interface Name

`LoadBalancerTargetServer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server |


# Example

```ts
import { LoadBalancerTargetServer } from 'hetzner-cloud-apilib';

const loadBalancerTargetServer: LoadBalancerTargetServer = {
  id: 80,
};
```



