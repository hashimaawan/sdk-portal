# Target

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlRhcmdldA

*This model accepts additional fields of type unknown.*


# Interface Name

`Target`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `healthStatus` | [`HealthStatus[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/health-status.md) | Optional | - |
| `server` | [`Server11 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-11.md) | Optional | - |
| `type` | `string \| undefined` | Optional | - |
| `usePrivateIp` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Status30, Target } from 'hetzner-cloud-apilib';

const target: Target = {
  healthStatus: [
    {
      listenPort: 142,
      status: Status30.Unknown,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      listenPort: 142,
      status: Status30.Unknown,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      listenPort: 142,
      status: Status30.Unknown,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  server: {
    id: 14,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  type: 'server',
  usePrivateIp: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



