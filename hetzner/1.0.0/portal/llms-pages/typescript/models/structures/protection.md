# Protection

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb3RlY3Rpb24

Protection configuration for the Resource


# Interface Name

`Protection`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean` | Required | If true, prevents the Resource from being deleted |


# Example

```ts
import { Protection } from 'hetzner-cloud-apilib';

const protection: Protection = {
  mDelete: false,
};
```



