# Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uSW5wdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetQueryExecutionInput } from 'amazon-athenalib';

const getQueryExecutionInput: GetQueryExecutionInput = {
  queryExecutionId: 'QueryExecutionId8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



