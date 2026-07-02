# Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`GetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetNamedQueryInput } from 'amazon-athenalib';

const getNamedQueryInput: GetNamedQueryInput = {
  namedQueryId: 'NamedQueryId8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



