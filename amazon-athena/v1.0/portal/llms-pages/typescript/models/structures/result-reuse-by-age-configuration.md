# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Interface Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean` | Required | - |
| `maxAgeInMinutes` | `number \| undefined` | Optional | **Constraints**: `>= 0`, `<= 10080` |


# Example

```ts
import { ResultReuseByAgeConfiguration } from 'amazon-athenalib';

const resultReuseByAgeConfiguration: ResultReuseByAgeConfiguration = {
  enabled: false,
  maxAgeInMinutes: 134,
};
```



