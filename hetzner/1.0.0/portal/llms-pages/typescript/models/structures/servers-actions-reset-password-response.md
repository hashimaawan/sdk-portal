# Servers Actions Reset Password Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMFJlc2V0JTI1MjBQYXNzd29yZCUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsResetPasswordResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `rootPassword` | `string \| undefined` | Optional | Password that will be set for this Server once the Action succeeds |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ServersActionsResetPasswordResponse,
  Status,
} from 'hetzner-cloud-apilib';

const serversActionsResetPasswordResponse: ServersActionsResetPasswordResponse = {
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
  rootPassword: 'zCWbFhnu950dUTko5f40',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



