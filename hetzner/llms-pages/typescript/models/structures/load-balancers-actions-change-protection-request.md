# Load Balancers Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Interface Name

`LoadBalancersActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Load Balancer from being deleted |


# Example

```ts
import {
  LoadBalancersActionsChangeProtectionRequest,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsChangeProtectionRequest: LoadBalancersActionsChangeProtectionRequest = {
  mDelete: true,
};
```



