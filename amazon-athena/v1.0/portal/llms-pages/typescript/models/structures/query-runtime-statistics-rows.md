# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.


# Interface Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `inputRows` | `number \| undefined` | Optional | - |
| `inputBytes` | `number \| undefined` | Optional | - |
| `outputBytes` | `number \| undefined` | Optional | - |
| `outputRows` | `number \| undefined` | Optional | - |


# Example

```ts
import { QueryRuntimeStatisticsRows } from 'amazon-athenalib';

const queryRuntimeStatisticsRows: QueryRuntimeStatisticsRows = {
  inputRows: 234,
  inputBytes: 254,
  outputBytes: 40,
  outputRows: 226,
};
```



