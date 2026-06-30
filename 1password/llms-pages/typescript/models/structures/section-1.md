# Section 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlNlY3Rpb24x

For files that are in a section, this field describes the section.

*This model accepts additional fields of type unknown.*


# Interface Name

`Section1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Section1 } from 'm-1-password-connectlib';

const section1: Section1 = {
  id: 'id2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



