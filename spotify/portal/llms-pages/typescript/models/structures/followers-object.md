# Followers Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkZvbGxvd2Vyc09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`FollowersObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string \| null \| undefined` | Optional | This will always be set to null, as the Web API does not support it at the moment. |
| `total` | `number \| undefined` | Optional | The total number of followers. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  FollowersObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const followersObject: FollowersObject = {
  href: 'href2',
  total: 62,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



