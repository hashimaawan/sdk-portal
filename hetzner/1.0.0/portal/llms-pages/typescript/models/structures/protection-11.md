# Protection 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb3RlY3Rpb24xMQ

Protection configuration for the Network


# Interface Name

`Protection11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean` | Required | If true, prevents the Network from being deleted |


# Example

```ts
import { Protection11 } from 'hetzner-cloud-apilib';

const protection11: Protection11 = {
  mDelete: false,
};
```



