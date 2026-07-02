# Result Reuse Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbg

Specifies the query result reuse behavior for the query.

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultReuseConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resultReuseByAgeConfiguration` | [`ResultReuseByAgeConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultReuseConfiguration } from 'amazon-athenalib';

const resultReuseConfiguration: ResultReuseConfiguration = {
  resultReuseByAgeConfiguration: {
    enabled: false,
    maxAgeInMinutes: 26,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



