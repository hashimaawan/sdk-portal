# Labels 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVsczI

User-defined labels (key-value pairs)

*This model accepts additional fields of type unknown.*


# Interface Name

`Labels2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelkey` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Labels2 } from 'hetzner-cloud-apilib';

const labels2: Labels2 = {
  labelkey: 'value',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



