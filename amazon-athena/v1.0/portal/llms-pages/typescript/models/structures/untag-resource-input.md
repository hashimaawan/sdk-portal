# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Interface Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tagKeys` | `string[]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```ts
import { UntagResourceInput } from 'amazon-athenalib';

const untagResourceInput: UntagResourceInput = {
  resourceARN: 'ResourceARN6',
  tagKeys: [
    'TagKeys1',
    'TagKeys2',
    'TagKeys3'
  ],
};
```



