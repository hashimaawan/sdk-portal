# Statistics 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXRpc3RpY3Mz

*This model accepts additional fields of type unknown.*


# Interface Name

`Statistics3`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dpuExecutionInMillis` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Statistics3 } from 'amazon-athenalib';

const statistics3: Statistics3 = {
  dpuExecutionInMillis: 130,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



