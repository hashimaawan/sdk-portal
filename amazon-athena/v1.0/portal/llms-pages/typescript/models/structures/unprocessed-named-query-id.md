# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.


# Interface Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `namedQueryId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `errorCode` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `errorMessage` | `string \| undefined` | Optional | - |


# Example

```ts
import { UnprocessedNamedQueryId } from 'amazon-athenalib';

const unprocessedNamedQueryId: UnprocessedNamedQueryId = {
  namedQueryId: 'NamedQueryId0',
  errorCode: 'ErrorCode8',
  errorMessage: 'ErrorMessage8',
};
```



