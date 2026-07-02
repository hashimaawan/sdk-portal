# Stop Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0b3BRdWVyeUV4ZWN1dGlvbklucHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`StopQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { StopQueryExecutionInput } from 'amazon-athenalib';

const stopQueryExecutionInput: StopQueryExecutionInput = {
  queryExecutionId: 'QueryExecutionId4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



