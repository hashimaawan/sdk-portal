# Section

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlNlY3Rpb24

*This model accepts additional fields of type unknown.*


# Interface Name

`Section`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Section } from 'm-1-password-connectlib';

const section: Section = {
  id: 'id6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



