# Label Selector 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I1

Configuration for type label_selector, required if type is `label_selector`

*This model accepts additional fields of type unknown.*


# Interface Name

`LabelSelector5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LabelSelector5 } from 'hetzner-cloud-apilib';

const labelSelector5: LabelSelector5 = {
  selector: 'env=prod',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



