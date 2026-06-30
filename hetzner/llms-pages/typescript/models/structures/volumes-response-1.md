# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ


# Interface Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Required | - |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Required | - |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/volume-1.md) | Required | - |


# Example

```ts
import {
  Status113Enum,
  StatusEnum,
  VolumesResponse1,
} from 'hetzner-cloud-apilib';

const volumesResponse1: VolumesResponse1 = {
  action: {
    command: 'start_server',
    error: {
      code: 'action_failed',
      message: 'Action failed',
    },
    finished: '2016-01-30T23:55:00+00:00',
    id: 42,
    progress: 100,
    resources: [
      {
        id: 42,
        type: 'server',
      }
    ],
    started: '2016-01-30T23:55:00+00:00',
    status: StatusEnum.Running,
  },
  nextActions: [
    {
      command: 'start_server',
      error: {
        code: 'action_failed',
        message: 'Action failed',
      },
      finished: '2016-01-30T23:55:00+00:00',
      id: 42,
      progress: 100,
      resources: [
        {
          id: 42,
          type: 'server',
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: StatusEnum.Success,
    }
  ],
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



