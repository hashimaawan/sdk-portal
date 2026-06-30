# Action

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkFjdGlvbg


# Interface Name

`Action`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `command` | `string` | Required | Command executed in the Action |
| `error` | [`Error \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/error.md) | Required | Error message for the Action if error occurred, otherwise null |
| `finished` | `string \| null` | Required | Point in time when the Action was finished (in ISO-8601 format). Only set if the Action is finished otherwise null. |
| `id` | `number` | Required | ID of the Resource |
| `progress` | `number` | Required | Progress of Action in percent |
| `resources` | [`Resource[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/resource.md) | Required | Resources the Action relates to |
| `started` | `string` | Required | Point in time when the Action was started (in ISO-8601 format) |
| `status` | [`StatusEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/status.md) | Required | Status of the Action |


# Example

```ts
import { Action, StatusEnum } from 'hetzner-cloud-apilib';

const action: Action = {
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
};
```



