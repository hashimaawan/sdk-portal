# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.


# Interface Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reusedPreviousResult` | `boolean` | Required | - |


# Example

```ts
import { ResultReuseInformation } from 'amazon-athenalib';

const resultReuseInformation: ResultReuseInformation = {
  reusedPreviousResult: false,
};
```



