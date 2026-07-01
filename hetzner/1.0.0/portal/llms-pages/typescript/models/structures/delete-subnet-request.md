# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q


# Interface Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string` | Required | IP range of subnet to delete |


# Example

```ts
import { DeleteSubnetRequest } from 'hetzner-cloud-apilib';

const deleteSubnetRequest: DeleteSubnetRequest = {
  ipRange: '10.0.1.0/24',
};
```



