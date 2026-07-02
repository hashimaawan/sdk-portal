# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `database` | [`Database2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/database-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetDatabaseOutput } from 'amazon-athenalib';

const getDatabaseOutput: GetDatabaseOutput = {
  database: {
    name: 'Name2',
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



