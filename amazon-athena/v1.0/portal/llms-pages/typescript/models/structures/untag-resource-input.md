# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `tagKeys` | `string[]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UntagResourceInput } from 'amazon-athenalib';

const untagResourceInput: UntagResourceInput = {
  resourceArn: 'ResourceARN6',
  tagKeys: [
    'TagKeys1',
    'TagKeys2',
    'TagKeys3'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



