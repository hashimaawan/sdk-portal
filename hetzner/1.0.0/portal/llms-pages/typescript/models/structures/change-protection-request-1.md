# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `mDelete` | `boolean \| undefined` | Optional | If true, prevents the Network from being deleted |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ChangeProtectionRequest1 } from 'hetzner-cloud-apilib';

const changeProtectionRequest1: ChangeProtectionRequest1 = {
  mDelete: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



