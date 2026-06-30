# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Interface Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |


# Example

```ts
import { ChangeTypeRequest } from 'hetzner-cloud-apilib';

const changeTypeRequest: ChangeTypeRequest = {
  loadBalancerType: 'lb21',
};
```



