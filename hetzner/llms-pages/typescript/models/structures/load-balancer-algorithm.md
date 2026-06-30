# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer


# Interface Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```ts
import { LoadBalancerAlgorithm, Type28Enum } from 'hetzner-cloud-apilib';

const loadBalancerAlgorithm: LoadBalancerAlgorithm = {
  type: Type28Enum.RoundRobin,
};
```



