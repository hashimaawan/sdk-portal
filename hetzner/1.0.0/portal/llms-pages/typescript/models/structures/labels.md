# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)

*This model accepts additional fields of type unknown.*


# Interface Name

`Labels`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labelkey` | `string \| undefined` | Optional | New label |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Labels } from 'hetzner-cloud-apilib';

const labels: Labels = {
  labelkey: 'value',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



