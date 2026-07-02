# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Class Name

`VolumesCreateBody`


# Cases

| Type |
|  --- |
| [`V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-volumes-request.md) |
| [`V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/v2-volumes-request-1.md) |


# V2VolumesRequest

## Initialization Code

### Example

```ts
const value: VolumesCreateBody = {
  name: 'example',
  sizeGigabytes: 10,
  region: Region2.Nyc3,
  createdAt: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  dropletIds: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshotId: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystemType: 'ext4',
};
```


# V2VolumesRequest1

## Initialization Code

### Example

```ts
const value: VolumesCreateBody = {
  name: 'example',
  sizeGigabytes: 10,
  region: Region2.Nyc3,
  createdAt: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  dropletIds: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshotId: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystemType: 'ext4',
};
```



