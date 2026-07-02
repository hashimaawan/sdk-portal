# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg


# Interface Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean` | Required | - |
| `maxAgeInMinutes` | `number \| undefined` | Optional | **Constraints**: `>= 0`, `<= 10080` |


# Example

```ts
import { ResultReuseByAgeConfiguration2 } from 'amazon-athenalib';

const resultReuseByAgeConfiguration2: ResultReuseByAgeConfiguration2 = {
  enabled: false,
  maxAgeInMinutes: 44,
};
```



