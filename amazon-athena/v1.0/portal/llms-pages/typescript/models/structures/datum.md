# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type unknown.*


# Interface Name

`Datum`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `varCharValue` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Datum } from 'amazon-athenalib';

const datum: Datum = {
  varCharValue: 'VarCharValue8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



