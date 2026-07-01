# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Interface Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `image` | [`Image \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/image.md) | Optional | - |


# Example

```ts
import {
  OsFlavorEnum,
  ServersActionsCreateImageResponse,
  Status24Enum,
  StatusEnum,
  Type22Enum,
} from 'hetzner-cloud-apilib';

const serversActionsCreateImageResponse: ServersActionsCreateImageResponse = {
  action: {
    command: 'command6',
    error: {
      code: 'code2',
      message: 'message4',
    },
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      {
        id: 198,
        type: 'type0',
      },
      {
        id: 198,
        type: 'type0',
      },
      {
        id: 198,
        type: 'type0',
      }
    ],
    started: 'started8',
    status: StatusEnum.Running,
  },
  image: {
    boundTo: 186,
    created: 'created6',
    createdFrom: {
      id: 60,
      name: 'name6',
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
    osFlavor: OsFlavorEnum.Debian,
    osVersion: 'os_version4',
    protection: {
      mDelete: false,
    },
    status: Status24Enum.Unavailable,
    type: Type22Enum.App,
    rapidDeploy: false,
  },
};
```



