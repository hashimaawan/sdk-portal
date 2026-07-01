# Load Balancers Actions Change Algorithm Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBBbGdvcml0aG0lMjUyMFJlcXVlc3Q


# Interface Name

`LoadBalancersActionsChangeAlgorithmRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type39Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-39.md) | Required | Algorithm of the Load Balancer |


# Example

```ts
import {
  LoadBalancersActionsChangeAlgorithmRequest,
  Type39Enum,
} from 'hetzner-cloud-apilib';

const loadBalancersActionsChangeAlgorithmRequest: LoadBalancersActionsChangeAlgorithmRequest = {
  type: Type39Enum.RoundRobin,
};
```



