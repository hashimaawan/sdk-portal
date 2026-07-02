# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2VolumesSnapshotsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `snapshot` | [`Snapshot \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/snapshot.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  ResourceType1,
  V2VolumesSnapshotsResponse,
} from 'digitalocean-apilib';

const v2VolumesSnapshotsResponse: V2VolumesSnapshotsResponse = {
  snapshot: {
    id: '8fa70202-873f-11e6-8b68-000f533176b1',
    createdAt: '2020-09-30T18:56:14Z',
    minDiskSize: 10,
    name: 'big-data-snapshot1475261774',
    regions: [
      'nyc1'
    ],
    sizeGigabytes: 10,
    resourceId: '82a48a18-873f-11e6-96bf-000f53315a41',
    resourceType: ResourceType1.Volume,
    tags: [
      'aninterestingtag'
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



