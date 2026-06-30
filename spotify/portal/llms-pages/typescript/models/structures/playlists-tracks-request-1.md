# Playlists Tracks Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0cyUyNTIwVHJhY2tzJTI1MjBSZXF1ZXN0MQ

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistsTracksRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `uris` | `string[] \| undefined` | Optional | - |
| `rangeStart` | `number \| undefined` | Optional | The position of the first item to be reordered. |
| `insertBefore` | `number \| undefined` | Optional | The position where the items should be inserted.<br/>To reorder the items to the end of the playlist, simply set _insert_before_ to the position after the last item.<br/>Examples:<br/>To reorder the first item to the last position in a playlist with 10 items, set _range_start_ to 0, and _insert_before_ to 10.<br/>To reorder the last item in a playlist with 10 items to the start of the playlist, set _range_start_ to 9, and _insert_before_ to 0. |
| `rangeLength` | `number \| undefined` | Optional | The amount of items to be reordered. Defaults to 1 if not set.<br/>The range of items to be reordered begins from the _range_start_ position, and includes the _range_length_ subsequent items.<br/>Example:<br/>To move the items at index 9-10 to the start of the playlist, _range_start_ is set to 9, and _range_length_ is set to 2. |
| `snapshotId` | `string \| undefined` | Optional | The playlist's snapshot ID against which you want to make the changes. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistsTracksRequest1,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistsTracksRequest1: PlaylistsTracksRequest1 = {
  uris: [
    'uris9'
  ],
  rangeStart: 1,
  insertBefore: 3,
  rangeLength: 2,
  snapshotId: 'snapshot_id4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



