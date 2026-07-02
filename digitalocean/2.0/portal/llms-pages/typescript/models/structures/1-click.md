# 1 Click

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRjFDbGljaw

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`M1Click`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `slug` | `string` | Required | The slug identifier for the 1-Click application. |
| `type` | `string` | Required | The type of the 1-Click application. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { M1Click } from 'digitalocean-apilib';

const m1Click: M1Click = {
  slug: 'monitoring',
  type: 'kubernetes',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



