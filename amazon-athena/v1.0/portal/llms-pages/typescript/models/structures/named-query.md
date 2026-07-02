# Named Query

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRk5hbWVkUXVlcnk

A query, where <code>QueryString</code> contains the SQL statements that make up the query.

*This model accepts additional fields of type unknown.*


# Interface Name

`NamedQuery`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `database` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `namedQueryId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { NamedQuery } from 'amazon-athenalib';

const namedQuery: NamedQuery = {
  name: 'Name8',
  database: 'Database0',
  queryString: 'QueryString4',
  description: 'Description4',
  namedQueryId: 'NamedQueryId0',
  workGroup: 'WorkGroup4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



