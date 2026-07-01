# Floating Ips Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMEFjdGlvbnMlMjUyMFJlc3BvbnNl


# Interface Name

`FloatingIpsActionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `actions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |


# Example

```ts
import { FloatingIpsActionsResponse, StatusEnum } from 'hetzner-cloud-apilib';

const floatingIpsActionsResponse: FloatingIpsActionsResponse = {
  actions: [
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
};
```



