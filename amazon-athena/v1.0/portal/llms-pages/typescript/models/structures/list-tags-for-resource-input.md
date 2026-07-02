# List Tags for Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`ListTagsForResourceInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resourceArn` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 75` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListTagsForResourceInput } from 'amazon-athenalib';

const listTagsForResourceInput: ListTagsForResourceInput = {
  resourceArn: 'ResourceARN0',
  nextToken: 'NextToken0',
  maxResults: 76,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



