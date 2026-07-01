# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVzZWRCeQ


# Interface Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of resource referenced |
| `type` | `string` | Required | Type of resource referenced |


# Example

```ts
import { UsedBy } from 'hetzner-cloud-apilib';

const usedBy: UsedBy = {
  id: 4711,
  type: 'load_balancer',
};
```



