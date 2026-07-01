# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeTypeRequest } from 'hetzner-cloud-apilib';

const changeTypeRequest: ChangeTypeRequest = {
  loadBalancerType: 'lb21',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



