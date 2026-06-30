# Markets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRk1hcmtldHM

*This model accepts additional fields of type unknown.*


# Interface Name

`Markets`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `markets` | `string[] \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  Markets,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const markets: Markets = {
  markets: [
    'CA',
    'BR',
    'IT'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



