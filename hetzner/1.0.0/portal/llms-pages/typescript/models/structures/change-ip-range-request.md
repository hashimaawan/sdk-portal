# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeIpRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ipRange` | `string` | Required | The new prefix for the whole Network |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeIpRangeRequest } from 'hetzner-cloud-apilib';

const changeIpRangeRequest: ChangeIpRangeRequest = {
  ipRange: '10.0.0.0/12',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



