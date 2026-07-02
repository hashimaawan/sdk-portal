# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ


# Interface Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `preparedStatements` | [`PreparedStatementSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ts
import { ListPreparedStatementsOutput } from 'amazon-athenalib';

const listPreparedStatementsOutput: ListPreparedStatementsOutput = {
  preparedStatements: [
    {
      statementName: 'StatementName2',
      lastModifiedTime: '2016-03-13T12:52:32.123Z',
    },
    {
      statementName: 'StatementName2',
      lastModifiedTime: '2016-03-13T12:52:32.123Z',
    }
  ],
  nextToken: 'NextToken2',
};
```



