# Load Balancer Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlckFsZ29yaXRobQ

Algorithm of the Load Balancer

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancerAlgorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type28`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-28.md) | Required | Type of the algorithm |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LoadBalancerAlgorithm, Type28 } from 'hetzner-cloud-apilib';

const loadBalancerAlgorithm: LoadBalancerAlgorithm = {
  type: Type28.RoundRobin,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



