# Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldE5hbWVkUXVlcnlJbnB1dA


# Interface Name

`GetNamedQueryInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```ts
import { GetNamedQueryInput } from 'amazon-athenalib';

const getNamedQueryInput: GetNamedQueryInput = {
  namedQueryId: 'NamedQueryId8',
};
```



