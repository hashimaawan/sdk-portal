# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Primary IP from being deleted |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeProtectionRequest2 } from 'hetzner-cloud-apilib';

const changeProtectionRequest2: ChangeProtectionRequest2 = {
  mDelete: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



