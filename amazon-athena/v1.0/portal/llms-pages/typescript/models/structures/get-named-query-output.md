# Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlPdXRwdXQ


# Interface Name

`GetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQuery` | [`NamedQuery1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/named-query-1.md) | Optional | - |


# Example

```ts
import { GetNamedQueryOutput } from 'amazon-athenalib';

const getNamedQueryOutput: GetNamedQueryOutput = {
  namedQuery: {
    name: 'Name0',
    database: 'Database8',
    queryString: 'QueryString2',
    description: 'Description6',
    namedQueryId: 'NamedQueryId2',
    workGroup: 'WorkGroup2',
  },
};
```



