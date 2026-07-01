# Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type unknown.*


# Interface Name

`VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `volume` | [`Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/volume-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Status, Status113, VolumesResponse1 } from 'hetzner-cloud-apilib';

const volumesResponse1: VolumesResponse1 = {
  action: {
    command: 'start_server',
    error: {
      code: 'action_failed',
      message: 'Action failed',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    finished: '2016-01-30T23:55:00+00:00',
    id: 42,
    progress: 100,
    resources: [
      {
        id: 42,
        type: 'server',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    started: '2016-01-30T23:55:00+00:00',
    status: Status.Running,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  nextActions: [
    {
      command: 'start_server',
      error: {
        code: 'action_failed',
        message: 'Action failed',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      finished: '2016-01-30T23:55:00+00:00',
      id: 42,
      progress: 100,
      resources: [
        {
          id: 42,
          type: 'server',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    name: 'my-resource',
    protection: {
      mDelete: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    server: 12,
    size: 42,
    status: Status113.Available,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



