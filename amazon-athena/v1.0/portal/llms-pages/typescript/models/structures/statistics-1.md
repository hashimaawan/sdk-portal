# Statistics 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mx

*This model accepts additional fields of type unknown.*


# Interface Name

`Statistics1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpuExecutionInMillis` | `number \| undefined` | Optional | - |
| `progress` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Statistics1 } from 'amazon-athenalib';

const statistics1: Statistics1 = {
  dpuExecutionInMillis: 148,
  progress: 'Progress4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



