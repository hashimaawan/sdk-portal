# Gif

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/#/typescript/x-redirect/JTI0bSUyRkdpZg


# Interface Name

`Gif`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `bitlyUrl` | `string \| undefined` | Optional | The unique bit.ly URL for this GIF |
| `contentUrl` | `string \| undefined` | Optional | Currently unused |
| `createDatetime` | `string \| undefined` | Optional | The date this GIF was added to the GIPHY database. |
| `embdedUrl` | `string \| undefined` | Optional | A URL used for embedding this GIF |
| `featuredTags` | `string[] \| undefined` | Optional | An array of featured tags for this GIF (Note: Not available when using the Public Beta Key) |
| `id` | `string \| undefined` | Optional | This GIF's unique ID |
| `images` | [`Images \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/typescript/models/structures/images.md) | Optional | An object containing data for various available formats and sizes of this GIF. |
| `importDatetime` | `string \| undefined` | Optional | The creation or upload date from this GIF's source. |
| `rating` | `string \| undefined` | Optional | The MPAA-style rating for this content. Examples include Y, G, PG, PG-13 and R |
| `slug` | `string \| undefined` | Optional | The unique slug used in this GIF's URL |
| `source` | `string \| undefined` | Optional | The page on which this GIF was found |
| `sourcePostUrl` | `string \| undefined` | Optional | The URL of the webpage on which this GIF was found. |
| `sourceTld` | `string \| undefined` | Optional | The top level domain of the source URL. |
| `tags` | `string[] \| undefined` | Optional | An array of tags for this GIF (Note: Not available when using the Public Beta Key) |
| `trendingDatetime` | `string \| undefined` | Optional | The date on which this gif was marked trending, if applicable. |
| `type` | [`TypeEnum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/typescript/models/enumerations/type.md) | Optional | Type of the gif. By default, this is almost always gif<br><br>**Default**: `TypeEnum.Gif` |
| `updateDatetime` | `string \| undefined` | Optional | The date on which this GIF was last updated. |
| `url` | `string \| undefined` | Optional | The unique URL for this GIF |
| `user` | [`User \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/llms-pages/typescript/models/structures/user.md) | Optional | The User Object contains information about the user associated with a GIF and URLs to assets such as that user's avatar image, profile, and more. |
| `username` | `string \| undefined` | Optional | The username this GIF is attached to, if applicable |


# Example

```ts
import { Gif, TypeEnum } from 'giphy-apilib';

const gif: Gif = {
  bitlyUrl: 'http://gph.is/1gsWDcL',
  contentUrl: 'content_url4',
  createDatetime: '2013-08-01 12:41:48',
  embdedUrl: 'http://giphy.com/embed/YsTs5ltWtEhnq',
  featuredTags: [
    'featured_tags0'
  ],
  id: 'YsTs5ltWtEhnq',
  importDatetime: '2013-08-01 12:41:48',
  rating: 'g',
  slug: 'confused-flying-YsTs5ltWtEhnq',
  source: 'http://www.reddit.com/r/reactiongifs/comments/1xpyaa/superman_goes_to_hollywood/',
  sourcePostUrl: 'http://cheezburger.com/5282328320',
  sourceTld: 'cheezburger.com',
  trendingDatetime: '2013-08-01 12:41:48',
  type: TypeEnum.Gif,
  updateDatetime: '2013-08-01 12:41:48',
  url: 'http://giphy.com/gifs/confused-flying-YsTs5ltWtEhnq',
  username: 'JoeCool4000',
};
```



