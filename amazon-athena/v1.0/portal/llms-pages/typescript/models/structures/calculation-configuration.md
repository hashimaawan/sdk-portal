# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type unknown.*


# Interface Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `codeBlock` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `68000` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CalculationConfiguration } from 'amazon-athenalib';

const calculationConfiguration: CalculationConfiguration = {
  codeBlock: 'CodeBlock2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



