# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`

*This model accepts additional fields of type unknown.*


# Interface Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selector` | `string` | Required | Label selector |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { LabelSelector1 } from 'hetzner-cloud-apilib';

const labelSelector1: LabelSelector1 = {
  selector: 'selector2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



