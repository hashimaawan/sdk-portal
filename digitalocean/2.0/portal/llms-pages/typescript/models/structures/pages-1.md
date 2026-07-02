# Pages 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2VzMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Pages1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first` | `string \| undefined` | Optional | URI of the first page of the results. |
| `prev` | `string \| undefined` | Optional | URI of the previous page of the results. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Pages1 } from 'digitalocean-apilib';

const pages1: Pages1 = {
  first: 'https://api.digitalocean.com/v2/images?page=1',
  prev: 'https://api.digitalocean.com/v2/images?page=1',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



