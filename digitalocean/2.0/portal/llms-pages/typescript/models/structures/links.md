# Links

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpbmtz

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Links`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pages` | [`LinksPages \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/oneof-anyof-definitions/links-pages.md) | Optional | This is a container for any-of cases. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Links } from 'digitalocean-apilib';

const links: Links = {
  pages: {
    last: 'last6',
    next: 'next2',
    additionalProperties: {
      'pages': { 'first': 'https: //api.digitalocean.com/v2/account/keys?page=1', 'prev': 'https: //api.digitalocean.com/v2/account/keys?page=2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



