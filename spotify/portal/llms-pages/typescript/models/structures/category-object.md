# Category Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkNhdGVnb3J5T2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`CategoryObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning full details of the category. |
| `icons` | [`ImageObject[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/llms-pages/typescript/models/structures/image-object.md) | Required | The category icon, in various sizes. |
| `id` | `string` | Required | The [Spotify category ID](/documentation/web-api/concepts/spotify-uris-ids) of the category. |
| `name` | `string` | Required | The name of the category. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CategoryObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const categoryObject: CategoryObject = {
  href: 'href2',
  icons: [
    {
      url: 'https://i.scdn.co/image/ab67616d00001e02ff9ca10b55ce82ae553c8228\n',
      height: 300,
      width: 300,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  id: 'equal',
  name: 'EQUAL',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



