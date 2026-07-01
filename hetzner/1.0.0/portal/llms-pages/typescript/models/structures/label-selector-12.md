# Label Selector 12

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3IxMg

Configuration for label selector targets, required if type is `label_selector`

*This model accepts additional fields of type unknown.*


# Interface Name

`LabelSelector12`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LabelSelector12 } from 'hetzner-cloud-apilib';

const labelSelector12: LabelSelector12 = {
  selector: 'env=prod',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



