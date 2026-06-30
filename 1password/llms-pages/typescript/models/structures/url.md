# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type unknown.*


# Interface Name

`Url`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | - |
| `label` | `string \| undefined` | Optional | - |
| `primary` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Url } from 'm-1-password-connectlib';

const url: Url = {
  href: 'href6',
  label: 'label4',
  primary: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



