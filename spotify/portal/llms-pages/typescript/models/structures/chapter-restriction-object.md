# Chapter Restriction Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRkNoYXB0ZXJSZXN0cmljdGlvbk9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`ChapterRestrictionObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `reason` | `string \| undefined` | Optional | The reason for the restriction. Supported values:<br><br>- `market` - The content item is not available in the given market.<br>- `product` - The content item is not available for the user's subscription type.<br>- `explicit` - The content item is explicit and the user's account is set to not play explicit content.<br>- `payment_required` - Payment is required to play the content item.<br><br>Additional reasons may be added in the future.<br>**Note**: If you use this field, make sure that your application safely handles unknown values. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ChapterRestrictionObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const chapterRestrictionObject: ChapterRestrictionObject = {
  reason: 'reason6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



