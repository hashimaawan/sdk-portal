# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of subnet to delete |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DeleteSubnetRequest } from 'hetzner-cloud-apilib';

const deleteSubnetRequest: DeleteSubnetRequest = {
  ipRange: '10.0.1.0/24',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



