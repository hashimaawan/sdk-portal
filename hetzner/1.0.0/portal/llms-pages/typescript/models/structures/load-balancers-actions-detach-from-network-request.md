# Load Balancers Actions Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwRGV0YWNoJTI1MjBGcm9tJTI1MjBOZXR3b3JrJTI1MjBSZXF1ZXN0


# Interface Name

`LoadBalancersActionsDetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `network` | `number` | Required | ID of an existing network to detach the Load Balancer from |


# Example

```ts
import {
  LoadBalancersActionsDetachFromNetworkRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsDetachFromNetworkRequest: LoadBalancersActionsDetachFromNetworkRequest = {
  network: 4711,
};
```



