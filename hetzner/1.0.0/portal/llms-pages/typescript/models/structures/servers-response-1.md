# Servers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersResponse1, Status } from 'hetzner-cloud-apilib';

const serversResponse1: ServersResponse1 = {
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



