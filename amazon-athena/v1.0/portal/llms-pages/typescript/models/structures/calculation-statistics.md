# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.

*This model accepts additional fields of type unknown.*


# Interface Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpuExecutionInMillis` | `number \| undefined` | Optional | - |
| `progress` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CalculationStatistics } from 'amazon-athenalib';

const calculationStatistics: CalculationStatistics = {
  dpuExecutionInMillis: 248,
  progress: 'Progress8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



