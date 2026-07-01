# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Interface Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string` | Required | The new prefix for the whole Network |


# Example

```ts
import { ChangeIPRangeRequest } from 'hetzner-cloud-apilib';

const changeIPRangeRequest: ChangeIPRangeRequest = {
  ipRange: '10.0.0.0/12',
};
```



