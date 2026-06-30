# Servers Actions Request Console Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlcXVlc3QlMjUyMENvbnNvbGUlMjUyMFJlc3BvbnNl


# Interface Name

`ServersActionsRequestConsoleResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/action.md) | Required | - |
| `password` | `string` | Required | VNC password to use for this connection (this password only works in combination with a wss_url with valid token) |
| `wssUrl` | `string` | Required | URL of websocket proxy to use; this includes a token which is valid for a limited time only |


# Example

```ts
import {
  ServersActionsRequestConsoleResponse,
  StatusEnum,
} from 'hetzner-cloud-apilib';

const serversActionsRequestConsoleResponse: ServersActionsRequestConsoleResponse = {
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
  password: '9MQaTg2VAGI0FIpc10k3UpRXcHj2wQ6x',
  wssUrl: 'wss://console.hetzner.cloud/?server_id=1&token=3db32d15-af2f-459c-8bf8-dee1fd05f49c',
};
```



