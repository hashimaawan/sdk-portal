# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA


# Interface Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueries` | [`NamedQuery[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/named-query.md) | Optional | - |
| `unprocessedNamedQueryIds` | [`UnprocessedNamedQueryId[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/unprocessed-named-query-id.md) | Optional | - |


# Example

```ts
import { BatchGetNamedQueryOutput } from 'amazon-athenalib';

const batchGetNamedQueryOutput: BatchGetNamedQueryOutput = {
  namedQueries: [
    {
      name: 'Name2',
      database: 'Database0',
      queryString: 'QueryString4',
      description: 'Description4',
      namedQueryId: 'NamedQueryId0',
      workGroup: 'WorkGroup4',
    },
    {
      name: 'Name2',
      database: 'Database0',
      queryString: 'QueryString4',
      description: 'Description4',
      namedQueryId: 'NamedQueryId0',
      workGroup: 'WorkGroup4',
    },
    {
      name: 'Name2',
      database: 'Database0',
      queryString: 'QueryString4',
      description: 'Description4',
      namedQueryId: 'NamedQueryId0',
      workGroup: 'WorkGroup4',
    }
  ],
  unprocessedNamedQueryIds: [
    {
      namedQueryId: 'NamedQueryId4',
      errorCode: 'ErrorCode6',
      errorMessage: 'ErrorMessage4',
    },
    {
      namedQueryId: 'NamedQueryId4',
      errorCode: 'ErrorCode6',
      errorMessage: 'ErrorMessage4',
    }
  ],
};
```



