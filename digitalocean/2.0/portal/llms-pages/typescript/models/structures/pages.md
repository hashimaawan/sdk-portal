# Pages

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2Vz

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Pages`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last` | `string \| undefined` | Optional | URI of the last page of the results. |
| `next` | `string \| undefined` | Optional | URI of the next page of the results. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Pages } from 'digitalocean-apilib';

const pages: Pages = {
  last: 'https://api.digitalocean.com/v2/images?page=2',
  next: 'https://api.digitalocean.com/v2/images?page=2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



