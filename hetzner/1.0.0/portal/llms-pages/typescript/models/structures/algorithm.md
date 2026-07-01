# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer


# Interface Name

`Algorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```ts
import { Algorithm, Type28Enum } from 'hetzner-cloud-apilib';

const algorithm: Algorithm = {
  type: Type28Enum.RoundRobin,
};
```



