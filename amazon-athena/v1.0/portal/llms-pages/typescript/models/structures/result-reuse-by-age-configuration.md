# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean` | Required | - |
| `maxAgeInMinutes` | `number \| undefined` | Optional | **Constraints**: `>= 0`, `<= 10080` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultReuseByAgeConfiguration } from 'amazon-athenalib';

const resultReuseByAgeConfiguration: ResultReuseByAgeConfiguration = {
  enabled: false,
  maxAgeInMinutes: 134,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



