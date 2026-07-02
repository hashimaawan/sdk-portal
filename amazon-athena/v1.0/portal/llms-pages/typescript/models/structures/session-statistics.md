# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.

*This model accepts additional fields of type unknown.*


# Interface Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpuExecutionInMillis` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { SessionStatistics } from 'amazon-athenalib';

const sessionStatistics: SessionStatistics = {
  dpuExecutionInMillis: 188,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



