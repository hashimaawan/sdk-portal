# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg


# Interface Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/volume-1.md) | Required | - |


# Example

```ts
import { Status113Enum, VolumesResponse2 } from 'hetzner-cloud-apilib';

const volumesResponse2: VolumesResponse2 = {
  volume: {
    created: '2016-01-30T23:55:00+00:00',
    format: 'xfs',
    id: 42,
    labels: {
      'key0': 'labels8',
      'key1': 'labels9',
      'key2': 'labels0'
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
  },
};
```



