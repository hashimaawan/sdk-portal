# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reusedPreviousResult` | `boolean` | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ResultReuseInformation } from 'amazon-athenalib';

const resultReuseInformation: ResultReuseInformation = {
  reusedPreviousResult: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



