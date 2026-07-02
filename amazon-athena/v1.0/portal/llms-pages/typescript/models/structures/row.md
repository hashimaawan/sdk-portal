# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.


# Interface Name

`Row`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `data` | [`Datum[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/datum.md) | Optional | - |


# Example

```ts
import { Row } from 'amazon-athenalib';

const row: Row = {
  data: [
    {
      varCharValue: 'VarCharValue8',
    }
  ],
};
```



