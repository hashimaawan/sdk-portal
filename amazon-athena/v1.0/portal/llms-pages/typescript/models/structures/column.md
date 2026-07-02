# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type unknown.*


# Interface Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `type` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `comment` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Column } from 'amazon-athenalib';

const column: Column = {
  name: 'Name6',
  type: 'Type6',
  comment: 'Comment2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



