# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg


# Interface Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Primary IP from being deleted |


# Example

```ts
import { ChangeProtectionRequest2 } from 'hetzner-cloud-apilib';

const changeProtectionRequest2: ChangeProtectionRequest2 = {
  mDelete: true,
};
```



