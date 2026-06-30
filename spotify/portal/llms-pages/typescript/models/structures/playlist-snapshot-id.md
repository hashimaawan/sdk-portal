# Playlist Snapshot Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRlBsYXlsaXN0U25hcHNob3RJZA

*This model accepts additional fields of type unknown.*


# Interface Name

`PlaylistSnapshotId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshotId` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PlaylistSnapshotId,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const playlistSnapshotId: PlaylistSnapshotId = {
  snapshotId: 'abc',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



