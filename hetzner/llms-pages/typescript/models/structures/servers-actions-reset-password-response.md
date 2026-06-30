# Servers Actions Reset Password Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlc2V0JTI1MjBQYXNzd29yZCUyNTIwUmVzcG9uc2U


# Interface Name

`ServersActionsResetPasswordResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `rootPassword` | `string \| undefined` | Optional | Password that will be set for this Server once the Action succeeds |


# Example

```ts
import {
  ServersActionsResetPasswordResponse,
  StatusEnum,
} from 'hetzner-cloud-apilib';

const serversActionsResetPasswordResponse: ServersActionsResetPasswordResponse = {
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
  rootPassword: 'zCWbFhnu950dUTko5f40',
};
```



