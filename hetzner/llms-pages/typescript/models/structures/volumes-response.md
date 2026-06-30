# Volumes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNl


# Interface Name

`VolumesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `volumes` | [`Volume1[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/volume-1.md) | Required | - |


# Example

```ts
import { Status113Enum, VolumesResponse } from 'hetzner-cloud-apilib';

const volumesResponse: VolumesResponse = {
  volumes: [
    {
      created: '2016-01-30T23:55:00+00:00',
      format: 'xfs',
      id: 42,
      labels: {
        'key0': 'labels4'
      },
      linuxDevice: '/dev/disk/by-id/scsi-0HC_Volume_4711',
      location: {
        city: 'Falkenstein',
        country: 'DE',
        description: 'Falkenstein DC Park 1',
        id: 1,
        latitude: 50.47612,
        longitude: 12.370071,
        name: 'fsn1',
        networkZone: 'eu-central',
      },
      name: 'my-resource',
      protection: {
        mDelete: false,
      },
      server: 12,
      size: 42,
      status: Status113Enum.Available,
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
    },
  },
};
```



