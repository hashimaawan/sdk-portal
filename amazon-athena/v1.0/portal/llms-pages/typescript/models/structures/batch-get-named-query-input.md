# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.


# Interface Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryIds` | `string[]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```ts
import { BatchGetNamedQueryInput } from 'amazon-athenalib';

const batchGetNamedQueryInput: BatchGetNamedQueryInput = {
  namedQueryIds: [
    'NamedQueryIds3',
    'NamedQueryIds4'
  ],
};
```



