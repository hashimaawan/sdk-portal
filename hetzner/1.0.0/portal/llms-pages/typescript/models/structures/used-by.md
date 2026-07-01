# Used By

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlVzZWRCeQ

*This model accepts additional fields of type unknown.*


# Interface Name

`UsedBy`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of resource referenced |
| `type` | `string` | Required | Type of resource referenced |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UsedBy } from 'hetzner-cloud-apilib';

const usedBy: UsedBy = {
  id: 4711,
  type: 'load_balancer',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



