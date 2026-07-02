# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0


# Interface Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `preparedStatement` | [`PreparedStatement1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/prepared-statement-1.md) | Optional | - |


# Example

```ts
import { GetPreparedStatementOutput } from 'amazon-athenalib';

const getPreparedStatementOutput: GetPreparedStatementOutput = {
  preparedStatement: {
    statementName: 'StatementName4',
    queryStatement: 'QueryStatement8',
    workGroupName: 'WorkGroupName8',
    description: 'Description0',
    lastModifiedTime: '2016-03-13T12:52:32.123Z',
  },
};
```



