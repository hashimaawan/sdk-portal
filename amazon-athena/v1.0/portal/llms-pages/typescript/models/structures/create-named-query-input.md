# Create Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlJbnB1dA

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CreateNamedQueryInput } from 'amazon-athenalib';

const createNamedQueryInput: CreateNamedQueryInput = {
  name: 'Name4',
  database: 'Database4',
  queryString: 'QueryString8',
  description: 'Description0',
  clientRequestToken: 'ClientRequestToken0',
  workGroup: 'WorkGroup8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



