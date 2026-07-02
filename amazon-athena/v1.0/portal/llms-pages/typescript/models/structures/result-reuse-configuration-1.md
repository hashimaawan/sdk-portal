# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE


# Interface Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resultReuseByAgeConfiguration` | [`ResultReuseByAgeConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |


# Example

```ts
import { ResultReuseConfiguration1 } from 'amazon-athenalib';

const resultReuseConfiguration1: ResultReuseConfiguration1 = {
  resultReuseByAgeConfiguration: {
    enabled: false,
    maxAgeInMinutes: 26,
  },
};
```



