# List Application DPU Sizes Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RBcHBsaWNhdGlvbkRQVVNpemVzSW5wdXQ


# Interface Name

`ListApplicationDPUSizesInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListApplicationDPUSizesInput } from 'amazon-athenalib';

const listApplicationDPUSizesInput: ListApplicationDPUSizesInput = {
  maxResults: 100,
  nextToken: 'NextToken8',
};
```



