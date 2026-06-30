# Servers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMQ


# Interface Name

`ServersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Optional | - |


# Example

```ts
import { ServersResponse1, StatusEnum } from 'hetzner-cloud-apilib';

const serversResponse1: ServersResponse1 = {
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
};
```



