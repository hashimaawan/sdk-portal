# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DeleteNamedQueryInput } from 'amazon-athenalib';

const deleteNamedQueryInput: DeleteNamedQueryInput = {
  namedQueryId: 'NamedQueryId4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



