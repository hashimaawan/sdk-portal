# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `databaseList` | [`Database[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/database.md) | Optional | - |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ListDatabasesOutput } from 'amazon-athenalib';

const listDatabasesOutput: ListDatabasesOutput = {
  databaseList: [
    {
      name: 'Name4',
      description: 'Description8',
      parameters: {
        additionalProperties: {
          'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'Name4',
      description: 'Description8',
      parameters: {
        additionalProperties: {
          'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'Name4',
      description: 'Description8',
      parameters: {
        additionalProperties: {
          'exampleAdditionalProperty': 'Parameters_additionalProperties2'
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  nextToken: 'NextToken6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



