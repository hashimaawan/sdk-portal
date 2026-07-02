# Filters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpbHRlcnM

*This model accepts additional fields of type unknown.*


# Interface Name

`Filters`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Filters } from 'amazon-athenalib';

const filters: Filters = {
  name: 'Name0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



