# Servers Actions Enable Rescue Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMEVuYWJsZSUyNTIwUmVzY3VlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsEnableRescueRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sshKeys` | `number[] \| undefined` | Optional | Array of SSH key IDs which should be injected into the rescue system. |
| `type` | [`Type65 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-65.md) | Optional | Type of rescue system to boot (default: `linux64`) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ServersActionsEnableRescueRequest,
  Type65,
} from 'hetzner-cloud-apilib';

const serversActionsEnableRescueRequest: ServersActionsEnableRescueRequest = {
  sshKeys: [
    2323
  ],
  type: Type65.Linux64,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



