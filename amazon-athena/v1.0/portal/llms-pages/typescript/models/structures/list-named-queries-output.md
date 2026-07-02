# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryIds` | `string[] \| undefined` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListNamedQueriesOutput } from 'amazon-athenalib';

const listNamedQueriesOutput: ListNamedQueriesOutput = {
  namedQueryIds: [
    'NamedQueryIds5',
    'NamedQueryIds4',
    'NamedQueryIds3'
  ],
  nextToken: 'NextToken2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



