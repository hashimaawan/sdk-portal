# Athena Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkF0aGVuYUVycm9yMg

*This model accepts additional fields of type unknown.*


# Interface Name

`AthenaError2`


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
import { AthenaError2 } from 'amazon-athenalib';

const athenaError2: AthenaError2 = {
  errorCategory: 3,
  errorType: 56,
  retryable: false,
  errorMessage: 'ErrorMessage0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



