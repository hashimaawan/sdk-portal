# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListApplicationDpuSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListApplicationDpuSizesInput } from 'amazon-athenalib';

const listApplicationDpuSizesInput: ListApplicationDpuSizesInput = {
  maxResults: 56,
  nextToken: 'NextToken6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



