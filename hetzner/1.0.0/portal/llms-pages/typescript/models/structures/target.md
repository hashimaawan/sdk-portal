# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlRhcmdldA


# Interface Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `healthStatus` | [`HealthStatus[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-11.md) | Optional | - |
| `type` | `string \| undefined` | Optional | - |
| `usePrivateIp` | `boolean \| undefined` | Optional | - |


# Example

```ts
import { Status30Enum, Target } from 'hetzner-cloud-apilib';

const target: Target = {
  healthStatus: [
    {
      listenPort: 142,
      status: Status30Enum.Unknown,
    },
    {
      listenPort: 142,
      status: Status30Enum.Unknown,
    },
    {
      listenPort: 142,
      status: Status30Enum.Unknown,
    }
  ],
  server: {
    id: 14,
  },
  type: 'server',
  usePrivateIp: false,
};
```



