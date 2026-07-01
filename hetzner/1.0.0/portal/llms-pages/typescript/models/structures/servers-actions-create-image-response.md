# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `image` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  OsFlavor,
  ServersActionsCreateImageResponse,
  Status,
  Status24,
  Type22,
} from 'hetzner-cloud-apilib';

const serversActionsCreateImageResponse: ServersActionsCreateImageResponse = {
  action: {
    command: 'command6',
    error: {
      code: 'code2',
      message: 'message4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    started: 'started8',
    status: Status.Running,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  image: {
    boundTo: 186,
    created: 'created6',
    createdFrom: {
      id: 60,
      name: 'name6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    deleted: 'deleted4',
    deprecated: 'deprecated8',
    description: 'description6',
    diskSize: 244.18,
    id: 128,
    imageSize: 141.34,
    labels: {
      'key0': 'labels4'
    },
    name: 'name6',
    osFlavor: OsFlavor.Debian,
    osVersion: 'os_version4',
    protection: {
      mDelete: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    status: Status24.Unavailable,
    type: Type22.App,
    rapidDeploy: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



