# External Id Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkV4dGVybmFsSWRPYmplY3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ExternalIdObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isrc` | `string \| undefined` | Optional | [International Standard Recording Code](http://en.wikipedia.org/wiki/International_Standard_Recording_Code) |
| `ean` | `string \| undefined` | Optional | [International Article Number](http://en.wikipedia.org/wiki/International_Article_Number_%28EAN%29) |
| `upc` | `string \| undefined` | Optional | [Universal Product Code](http://en.wikipedia.org/wiki/Universal_Product_Code) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ExternalIdObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const externalIdObject: ExternalIdObject = {
  isrc: 'isrc4',
  ean: 'ean2',
  upc: 'upc6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



