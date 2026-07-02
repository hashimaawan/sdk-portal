# Start Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`StartQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { StartQueryExecutionOutput } from 'amazon-athenalib';

const startQueryExecutionOutput: StartQueryExecutionOutput = {
  queryExecutionId: 'QueryExecutionId0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



