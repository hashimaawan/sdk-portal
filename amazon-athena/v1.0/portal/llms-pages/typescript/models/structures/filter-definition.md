# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.

*This model accepts additional fields of type unknown.*


# Interface Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { FilterDefinition } from 'amazon-athenalib';

const filterDefinition: FilterDefinition = {
  name: 'Name2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



