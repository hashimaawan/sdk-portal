# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I

*This model accepts additional fields of type unknown.*


# Interface Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LabelSelector } from 'hetzner-cloud-apilib';

const labelSelector: LabelSelector = {
  selector: 'env=prod',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



