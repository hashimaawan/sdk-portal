# Get Query Runtime Statistics Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5UnVudGltZVN0YXRpc3RpY3NJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`GetQueryRuntimeStatisticsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetQueryRuntimeStatisticsInput } from 'amazon-athenalib';

const getQueryRuntimeStatisticsInput: GetQueryRuntimeStatisticsInput = {
  queryExecutionId: 'QueryExecutionId0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



