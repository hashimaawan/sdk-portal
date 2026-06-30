# Load Balancers Actions Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQXR0YWNoJTI1MjBUbyUyNTIwTmV0d29yayUyNTIwUmVxdWVzdA


# Interface Name

`LoadBalancersActionsAttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ip` | `string \| undefined` | Optional | IP to request to be assigned to this Load Balancer; if you do not provide this then you will be auto assigned an IP address |
| `network` | `number` | Required | ID of an existing network to attach the Load Balancer to |


# Example

```ts
import {
  LoadBalancersActionsAttachToNetworkRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsAttachToNetworkRequest: LoadBalancersActionsAttachToNetworkRequest = {
  network: 4711,
  ip: '10.0.1.1',
};
```



