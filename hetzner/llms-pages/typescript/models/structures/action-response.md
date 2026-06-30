# Action Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkFjdGlvblJlc3BvbnNl


# Interface Name

`ActionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Required | - |


# Example

```ts
import { ActionResponse, StatusEnum } from 'hetzner-cloud-apilib';

const actionResponse: ActionResponse = {
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
};
```



