# Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0


# Interface Name

`ChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Floating IP from being deleted |


# Example

```ts
import { ChangeProtectionRequest } from 'hetzner-cloud-apilib';

const changeProtectionRequest: ChangeProtectionRequest = {
  mDelete: true,
};
```



