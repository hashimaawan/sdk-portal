# Athena Error

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkF0aGVuYUVycm9y

Provides information about an Athena query error. The <code>AthenaError</code> feature provides standardized error information to help you understand failed queries and take steps after a query failure occurs. <code>AthenaError</code> includes an <code>ErrorCategory</code> field that specifies whether the cause of the failed query is due to system error, user error, or other error.

*This model accepts additional fields of type unknown.*


# Interface Name

`AthenaError`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `errorCategory` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 3` |
| `errorType` | `number \| undefined` | Optional | **Constraints**: `>= 0`, `<= 9999` |
| `retryable` | `boolean \| undefined` | Optional | - |
| `errorMessage` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { AthenaError } from 'amazon-athenalib';

const athenaError: AthenaError = {
  errorCategory: 3,
  errorType: 238,
  retryable: false,
  errorMessage: 'ErrorMessage0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



