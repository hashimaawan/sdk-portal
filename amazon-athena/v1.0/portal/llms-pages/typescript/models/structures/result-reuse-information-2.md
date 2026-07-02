# Result Reuse Information 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24y

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultReuseInformation2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reusedPreviousResult` | `boolean` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultReuseInformation2 } from 'amazon-athenalib';

const resultReuseInformation2: ResultReuseInformation2 = {
  reusedPreviousResult: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



