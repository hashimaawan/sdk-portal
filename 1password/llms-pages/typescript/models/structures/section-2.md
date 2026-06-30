# Section 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlNlY3Rpb24y

*This model accepts additional fields of type unknown.*


# Interface Name

`Section2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | - |
| `label` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Section2 } from 'm-1-password-connectlib';

const section2: Section2 = {
  id: 'id4',
  label: 'label4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



