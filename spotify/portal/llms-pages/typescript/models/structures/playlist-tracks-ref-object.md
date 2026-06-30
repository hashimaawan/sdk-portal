# Playlist Tracks Ref Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0VHJhY2tzUmVmT2JqZWN0

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistTracksRefObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint where full details of the playlist's tracks can be retrieved. |
| `total` | `number \| undefined` | Optional | Number of tracks in the playlist. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistTracksRefObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistTracksRefObject: PlaylistTracksRefObject = {
  href: 'href6',
  total: 80,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



